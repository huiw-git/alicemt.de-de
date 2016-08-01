---
title: "Verwenden von „Immer verschl&#252;sselt“ mit dem JDBC-Treiber"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 271c0438-8af1-45e5-b96a-4b1cabe32707
caps.latest.revision: 47
caps.handback.revision: 14
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Verwenden von „Immer verschl&#252;sselt“ mit dem JDBC-Treiber
  „Immer verschlüsselt“ ermöglicht es Clients, sensible Daten in Clientanwendungen zu verschlüsseln und die Verschlüsselungsschlüssel niemals an SQL Server weiterzugeben. Ein auf dem Clientcomputer installierter Treiber, bei dem „Immer verschlüsselt“ aktiviert ist, erreicht dies durch die automatische Ver\- und Entschlüsselung von sensiblen Daten in der SQL Server\-Clientanwendung. Der Treiber verschlüsselt die Daten in vertraulichen Spalten, bevor er sie an SQL Server weitergibt, und schreibt Abfragen automatisch neu, sodass die Semantik der Anwendung beibehalten wird. Auf ähnliche Weise entschlüsselt der Treiber transparent Daten in verschlüsselten Datenbankspalten, die in Abfrageergebnissen enthalten sind. Weitere Informationen finden Sie unter [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
 **Einschränkungen der Vorschauversion**  
  
> [!NOTE]  
>  „Immer verschlüsselt“ wird nur von Microsoft JDBC Driver 6.0 \(Vorschau\) für SQL Server mit SQL Server 2016 \(Vorschau\) unterstützt. Diese Vorschauversion unterstützt Folgendes **nicht**:  
>   
>  -   Massenkopieren  
> -   XA\-Transaktionen  
> -   In der Linux\-Clientumgebung ist die Unterstützung nicht sprachübergreifend. Daten, die vom JDBC\-Treiber verschlüsselt wurden, können nur vom JDBC\-Treiber entschlüsselt werden und umgekehrt.  
> -   Ausgabeparameter und Rückgabetypen von gespeicherten Prozeduren  
> -   Java Runtime Environments \(JRE\), die von anderen Quellen als der Oracle Corporation bereitgestellt wurden  
  
## Entwickeln von Clientanwendungen, um auf immer verschlüsselte Daten zuzugreifen  
 Das Abfragen einer Datenbank mit „Immer verschlüsselt“ von einer Clientanwendung aus erfordert minimalen Entwicklungsaufwand. Im Folgenden werden die  Komponenten und Maßnahmen zusammengefasst, die erforderlich sind, damit Ihre Anwendung immer verschlüsselte Daten lesen und schreiben kann.  
  
### Erforderliche Komponenten  
  
-   Konfigurieren Sie den Server gemäß der Anweisungen im Abschnitt **Erste Schritte mit „Immer verschlüsselt“** des Themas [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
-   Installieren Sie den **Microsoft JDBC Driver 6.0 für SQL Server \(Vorschau\)** auf dem Clientcomputer.  
  
-   Laden Sie die Richtliniendateien Java Cryptography Extension \(JCE\) Unlimited Strength Jurisdiction herunter und installieren Sie sie.  Achten Sie darauf, die in der ZIP\-Datei enthaltene Infodatei zu lesen, um Installationsanweisungen und relevante Details zu möglichen Export\-\/Importproblemen zu erhalten.  
  
    -   Wenn Sie die Datei sqljdbc41.jar verwenden, können die Richtliniendateien von [Java Cryptography Extension \(JCE\) Unlimited Strength Jurisdiction Policy Files 7 Download](http://www.oracle.com/technetwork/java/javase/downloads/jce-7-download-432124.html) heruntergeladen werden.  
  
    -   Wenn Sie die Datei sqljdbc42.jar verwenden, können die Richtliniendateien von [Java Cryptography Extension \(JCE\) Unlimited Strength Jurisdiction Policy Files 8 Download](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html) heruntergeladen werden.  
  
### Einrichten der Clientanwendung  
 Die Clientanwendung muss so konfiguriert sein, dass sie Zugriff auf einen Schlüsselspeicher hat, der einen Spaltenhauptschlüssel \(Column Master Key, CMK\) enthält. Dieser schützt die Daten, auf die die Anwendung zugreift. Weitere Informationen zu Hauptschlüsseln finden Sie unter [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx). Der JDBC\-Treiber unterstützt das Speichern von CMKs beim Anbieter JVM Key Store und bei benutzerdefinierten Anbietern.  
  
### Verwenden des Java Virtual Machine \(JVM\)\-Schlüsselspeicheranbieters  
 Der JDBC\-Treiber ist mit einer integrierten Schlüsselspeicheranbieter\-Implementierung für JVM Key Store ausgestattet. Clientanwendungen müssen den Anbieter instanziieren, indem sie die JVM\-Anmeldeinformationen für den Schlüsselspeicher einreichen und den Anbieter beim Treiber registrieren. Der Name des JVM\-Schlüsselspeicheranbieters ist MSSQL\_JVM\_KEYSTORE. \(Hinweis: Das Präfix MSSQL\_ für Namen von Schlüsselspeicheranbietern ist für Systemanbieter reserviert. Benutzer können nur MSSQL\_JVM\_KEYSTORE registrieren, wenn das Präfix MSSQL\_ verwendet wird.\) Die erforderlichen Anmeldedaten sind der JVM\-Schlüsselspeicherpfad, das JVM\-Schlüsselspeicherkennwort und die Kennwörter für die privaten Schlüssel der Zertifikate, die mit „Immer verschlüsselt“ werden sollen.  
  
 Dies ist der Konstruktor, um JVM Key Store zu instanziieren:  
  
```  
public SQLServerColumnEncryptionJVMKeyStoreProvider( String keyStorePath, char[] keyStorePassword, Map<String, char[]> certificatePasswords)  
  
```  
  
 **keyStorePath:** Der Pfad zu JVM Key Store  
  
 **keyStorePassword:** Das Kennwort von JVM Key Store  
  
 **certificatePasswords:** Eine Zuordnung vom CMK\-Pfad zum Kennwort des entsprechenden privaten Schlüssels des Zertifikats, das in der CMK\-Definition verwendet wird. Dieser Pfad muss \(bei Beachtung der Groß\-\/Kleinschreibung\) genau mit dem Pfad übereinstimmen, der in der CMK\-Definition verwendet wird. Diese Zuordnung sollte die Kennwörter für alle Zertifikate enthalten, die mit „Immer verschlüsselt“ verwendet werden sollen.  
  
> [!NOTE]  
>  Die Vorschauversion von Microsoft JDBC Driver 6.0 unterstützt den Windows\-Zertifikatspeicher nicht.  
  
### Erstellen eines Spaltenhauptschlüssels \(Column Master Key, CMK\) für JVM Key Store  
 Der Anbieter JVM Key Store akzeptiert entweder den Fingerabdruck eines Zertifikats oder einen Zertifikatsalias als CMK\-Pfad. Der Name des Anbieters muss „MSSQL\_JVM\_KEYSTORE“ sein. Das Format der CMK\-Definition lautet wie folgt:  
  
```  
CREATE COLUMN MASTER KEY [MYCMK] WITH ( KEY_STORE_PROVIDER_NAME = N'MSSQL_JVM_KEYSTORE', KEY_PATH = N'Thumbprint:<certificate_thumbprint>' )  
  
```  
  
 OR  
  
```  
CREATE COLUMN MASTER KEY [MYCMK] WITH ( KEY_STORE_PROVIDER_NAME = N'MSSQL_JVM_KEYSTORE', KEY_PATH = N'Alias:<certificate_alias>' )  
  
```  
  
> [!NOTE]  
>  Durch das Verwenden eines CMK mit einem Alias in KEY\_PATH wird eine besser Leistung erzielt als durch das Verwenden eines CMK mit einem Fingerabdruck in KEY\_PATH.  
>   
>  Die integrierte SQL Server Management Studio\-Funktionalität erstellt CMK\-Definitionen nur für den Windows\-Zertifikatspeicher. Um die CMK\-Definition für JVM Key Store zu erstellen, müssen Sie die Abfrage stattdessen direkt ausführen.  
  
### Erstellen eines Spaltenverschlüsselungsschlüssels \(Column Encryption Key, CEK\) für JVM Key Store  
 Die Methode SQLServerColumnEncryptionJVMKeyStoreProvider.encryptColumnEncryptionKey\(\) kann verwendet werden, um einen vom Nutzer bereitgestellten Klartext\-CEK zu verschlüsseln. Diese Methode verwendet den CMK\-Pfad \(Hinweis: der CMK muss in JVM Key Store sein\), den Algorithmus \(der einzige akzeptierte Algorithmus ist „RSA\_OAEP“\) und den Klartext\-CEK\-Wert, und gibt den verschlüsselten CEK zurück. Eine CEK kann darauf in SQL Server mithilfe des T\-SQL\-Befehls erstellt werden, wie in [CREATE COLUMN ENCRYPTION KEY](https://msdn.microsoft.com/en-CA/library/mt146372.aspx) beschrieben. Unten finden Sie Beispielcode zum Erstellen eines CEK. Dieser ist auch im Beispielverzeichnis des Downloadpakets enthalten.  
  
```  
import java.sql.*; import java.util.HashMap; import java.util.Map; import javax.xml.bind.DatatypeConverter; import com.microsoft.sqlserver.jdbc.SQLServerColumnEncryptionJVMKeyStoreProvider; import com.microsoft.sqlserver.jdbc.SQLServerColumnEncryptionKeyStoreProvider; import com.microsoft.sqlserver.jdbc.SQLServerException; /** * This class demonstrates how to create CMK and CEK * CMK is created first and then it is used to create CEK */ public class AlwaysEncrypted { /** *  Specifies the name of a key store provider , for JVM *  system provider use MSSQL_JVM_KEYSTORE */ private static String keyStoreProviderName = "MSSQL_JVM_KEYSTORE"; /** Specified details of the certificate to be used by Always Encrypted * User can choose from the following two option * 1. "Thumbprint:<Thumbprint of the certificate>" * 2. "Alias :<Alias of the certificate>" */ private static String key_Path_Thumbprint = "Thumbprint:<Thumprint of certificate>"; // Name by which the column master key will be known in the database. private static String columnMasterKeyName = "JDBC_CMK"; // Name by which the column encryption key will be known in the database. private static String columnEncryptionKey = "JDBC_CEK"; /** * Name of the encryption algorithm used to encrypt the value of * the column encryption key. The algorithm for the system providers must be RSA_OAEP. */ private static String algorithm = "RSA_OAEP"; public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet objects that you create. // Open a sourceConnection to the database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { /** * Create column mater key * For details on syntax  refer: * https://msdn.microsoft.com/en-CA/library/mt146393.aspx * */ String createCMKSQL = "CREATE COLUMN MASTER KEY " + columnMasterKeyName + " WITH ( " + " KEY_STORE_PROVIDER_NAME = '" + keyStoreProviderName + "' , KEY_PATH =  '" + key_Path_Thumbprint + "' ) "; try (Statement cmkStatement = sourceConnection.createStatement()) { cmkStatement.executeUpdate(createCMKSQL); System.out.println("Column Master Key created with name : " + columnMasterKeyName); } byte [] encryptedCEK=getEncryptedCEK(); /** * Create column encryption key * For more details on the syntax refer: * https://msdn.microsoft.com/en-CA/library/mt146372.aspx * Encrypted CEK first needs to be converted into varbinary_literal from bytes, * for which DatatypeConverter.printHexBinary is used */ String createCEKSQL = "CREATE COLUMN ENCRYPTION KEY " + columnEncryptionKey + " WITH VALUES ( " + " COLUMN_MASTER_KEY = " + columnMasterKeyName + " , ALGORITHM =  '" + algorithm + "' , ENCRYPTED_VALUE =  0x" + DatatypeConverter.printHexBinary(encryptedCEK) + " ) "; try (Statement cekStatement = sourceConnection.createStatement()) { cekStatement.executeUpdate(createCEKSQL); System.out.println("CEK created with name : " + columnEncryptionKey); } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=ae;user=sa;password=****;"; return connectionUrl; } private static byte[] getEncryptedCEK() throws SQLServerException { // This map contains certificates and passwords Map<String, char[]> certPwds = new HashMap<String, char[]>(); // Thumbprint/Alias of certificate and password of associated private key certPwds.put(key_Path_Thumbprint, "password".toCharArray()); /** * Following arguments needed by  SQLServerColumnEncryptionJVMKeyStoreProvider * 1) keyStorePath : * 		Path where keystore is located. If null is provided default cacerts keystore is used * 2) keyStorePassword : * 		Password of the keystore. * 3) Map<String,char[]> : * 		Map of the certificate identifiers like thumbprint/alias and password for the corresponding private key */ SQLServerColumnEncryptionKeyStoreProvider storeProvider = new SQLServerColumnEncryptionJVMKeyStoreProvider( null, "password".toCharArray(), certPwds); String plainTextKey = "You need to give your plain text"; // plainTextKey has to be 32 bytes with current algorithm supported byte[] plainCEK = plainTextKey.getBytes(); // This will give us encrypted column encryption key in bytes byte[] encryptedCEK = storeProvider.encryptColumnEncryptionKey( key_Path_Thumbprint, algorithm, plainCEK); return encryptedCEK; } }  
  
```  
  
> [!NOTE]  
>  Die integrierte SQL Server Management Studio\-Funktionalität erstellt CEKs mithilfe von CMKs nur im Windows\-Zertifikatspeicher. Wenn der CM in JVM Key Store ist, verwenden Sie die im Beispielcode oben beschriebene Methode, um stattdessen einen CEK zu erstellen.  
  
### Erstellen von sprachübergreifenden CEKs  
 Clientanwendungen können mithilfe mehrerer Clienttreiber in einer Tabelle auf die verschlüsselte Spalte zugreifen. Beispielsweise kann eine Spalte, die vom JDBC\-Treiber verschlüsselt wurde, von einem ADO.NET\-Treiber entschlüsselt werden und umgekehrt. Die Voraussetzung für diese sprachübergreifende Kompatibilität ist, dass alle Treiber Zugriff auf mindestens einen CMK haben, der zum Verschlüsseln des CEK verwendet wird. Bei der Verwendung benutzerdefinierter Schlüsselspeicheranbieter muss der gleiche Anbieter für beide Treiber implementiert und registriert werden oder der CEK sollte über zwei CMK\-Definitionen verfügen, eine für jeden Treiber. Wenn Sie System\-Schlüsselspeicheranbieter verwenden, sollte der CEK für den JDBC\-Treiber mithilfe eines CMK von JVM Key Store und für andere Treiber mithilfe eines CMK des Windows\-Zertifikatspeichers verschlüsselt werden. Beachten Sie , dass für den JDBC\-Treiber \(Vorschau\) eine CMK\-Rotation nicht möglich ist, wenn ein CEK sprachübergreifend ist.  
  
 Wenn verschiedene Zertifikate für JVM Key Store und für den Windows\-Zertifikatspeicher verwendet werden, müssen Benutzer zwei CMKs für diese beiden Zertifikate erstellen sowie einen CEK mit Werten, die von beiden CMKs verschlüsselt wurden.  
  
 Alternativ kann ein Benutzer ein Zertifikat des Windows\-Zertifikatspeichers nach JVM Key Store importieren und mit dem gleichen Zertifikat CMK\-Definitionen für beide Anbieter erstellen. Der verschlüsselte Wert des CEK wird in diesem Fall für beide Anbieter gleich sein, da sie dasselbe Zertifikat verwenden. Ist der Fingerabdruck für dieses Zertifikat beispielsweise „f2260f28d909d21c642a3d8e0b45a830e79a1420“, sieht die CMK\-Definition folgendermaßen aus:  
  
```  
CREATE COLUMN MASTER KEY [CmkJvmKeyStore] WITH ( KEY_STORE_PROVIDER_NAME = N'MSSQL_JVM_KEYSTORE', KEY_PATH = N'Thumbprint:f2260f28d909d21c642a3d8e0b45a830e79a1420' ) CREATE COLUMN MASTER KEY [CmkWindowsCertificateStore] WITH ( KEY_STORE_PROVIDER_NAME = N'MSSQL_CERTIFICATE_STORE', KEY_PATH = N' Current User/Personal/f2260f28d909d21c642a3d8e0b45a830e79a1420' )  
  
```  
  
 Beachten Sie, dass in beiden CMK\-Definitionen der gleiche Fingerabdruck verwendet wird.  
  
 Da das Zertifikat im Windows\-Zertifikatspeicher verfügbar ist, kann der CEK mithilfe von SQL Server Management Studio erstellt werden, mit einem vom CMK verschlüsselten Wert, **CmkWindowsCertificateStore**. Der Benutzer kann den CEK mithilfe des T\-SQL\-Befehls [ALTER COLUMN ENCRYPTION KEY](https://msdn.microsoft.com/en-CA/library/mt146388.aspx) bearbeiten, um einen weiteren vom CMK verschlüsselten Wert hinzuzufügen, **CmkJvmKeyStore**. Der verschlüsselte Wert wäre für beide Werte identisch, da sie mit demselben Zertifikat und demselben Algorithmus verschlüsselt wurden. Der CEK würde folgendermaßen aussehen:  
  
```  
CREATE COLUMN ENCRYPTION KEY [CekCrossLanguage] WITH VALUES ( COLUMN COLUMN_MASTER MASTER_KEY DEFINITION = CmkWindowsCertificateStore, ALGORITHM = 'RSA_OAEP', ENCRYPTED_VALUE = 0x016E000001630075007200720065006E00740075007300650072002F006D0079002F0037006300380061003100310033003400320037003800620037003000630038003100390062003900630039003400360061006600340039006500610030003200650038006200650038003400340065006C33A82ECF04A7185824B4545457AC5244CD9C219E64067B9520C0081B8399B58C2863F7494ABE3694BD87D55FFD7576FFDC47C28F94ECC99577DF4FB8FA19AA95764FEF889CDE0F176DA5897B74382FBB22756CE2921050A09201A0EB6AF3D6091014C30146EA62635EE8CBF0A8074DEDFF125CEA80D1C0F5E8C58750A07D270E2A8BF824EE4C0C156366BF26D38CCE49EBDD5639A2DF029A7DBAE5A5D111F2F2FA3246DF8C2FA83C1E542C10570FADA98F6B29478DC58CE5CBDD407CCEFCDB97814525F6F32BECA266014AC346AC39C4F185C6C0F0A24FEC4DFA015649624692DE7865B9827BA22C3B574C9FD169F822B609F902288C5880EB25F14BD990D871B1BC4BA3A5B237AF76D26354773FA2A25CF4511AF58C911E601CFCB1905128C997844EED056C2AE7F0B48700AB41307E470FF9520997D0EB0D887DE11AFE574FFE845B7DC6C03FEEE8D467236368FC0CB2FDBD54DADC65B10B3DE6C80DF8B7B3F8F3CE5BE914713EE7B1FA5B7A578359592B8A5FDFDDE5FF9F392BC87C3CD02FBA94582AC063BBB9FFAC803FD489E16BEB28C4E3374A8478C737236A0B232F5A9DDE4D119573F1AEAE94B2192B81575AD6F57E670C1B2AB91045124DFDAEC2898F3F0112026DFC93BF9391D667D1AD7ED7D4E6BB119BBCEF1D1ADA589DD3E1082C3DAD13223BE438EB9574DA04E9D8A06320CAC6D3EC21D5D1C2A0AA484C7C ), ( COLUMN COLUMN_MASTER MASTER_KEY DEFINITION = CmkJvmKeyStore, ALGORITHM = 'RSA_OAEP', ENCRYPTED_VALUE = 0x016E000001630075007200720065006E00740075007300650072002F006D0079002F0037006300380061003100310033003400320037003800620037003000630038003100390062003900630039003400360061006600340039006500610030003200650038006200650038003400340065006C33A82ECF04A7185824B4545457AC5244CD9C219E64067B9520C0081B8399B58C2863F7494ABE3694BD87D55FFD7576FFDC47C28F94ECC99577DF4FB8FA19AA95764FEF889CDE0F176DA5897B74382FBB22756CE2921050A09201A0EB6AF3D6091014C30146EA62635EE8CBF0A8074DEDFF125CEA80D1C0F5E8C58750A07D270E2A8BF824EE4C0C156366BF26D38CCE49EBDD5639A2DF029A7DBAE5A5D111F2F2FA3246DF8C2FA83C1E542C10570FADA98F6B29478DC58CE5CBDD407CCEFCDB97814525F6F32BECA266014AC346AC39C4F185C6C0F0A24FEC4DFA015649624692DE7865B9827BA22C3B574C9FD169F822B609F902288C5880EB25F14BD990D871B1BC4BA3A5B237AF76D26354773FA2A25CF4511AF58C911E601CFCB1905128C997844EED056C2AE7F0B48700AB41307E470FF9520997D0EB0D887DE11AFE574FFE845B7DC6C03FEEE8D467236368FC0CB2FDBD54DADC65B10B3DE6C80DF8B7B3F8F3CE5BE914713EE7B1FA5B7A578359592B8A5FDFDDE5FF9F392BC87C3CD02FBA94582AC063BBB9FFAC803FD489E16BEB28C4E3374A8478C737236A0B232F5A9DDE4D119573F1AEAE94B2192B81575AD6F57E670C1B2AB91045124DFDAEC2898F3F0112026DFC93BF9391D667D1AD7ED7D4E6BB119BBCEF1D1ADA589DD3E1082C3DAD13223BE438EB9574DA04E9D8A06320CAC6D3EC21D5D1C2A0AA484C7C );  
  
```  
  
 Beachten Sie, dass die verschlüsselte CEK\-BLOB\-Datei für beide Werte identisch ist, da der CEK mit demselben Zertifikat verschlüsselt wurde, das sich in zwei Speichern befindet.  
  
### Aktivieren von „Immer verschlüsselt“ für eine Clientverbindung  
 Ändern Sie die Verbindungszeichenfolge in der Clientanwendung, indem Sie den Parameter columnEncryptionSetting\=true zur Verbindungszeichenfolge hinzufügen.  
  
 Im Folgenden finden Sie ein Beispiel für eine Verbindungszeichenfolge für Microsoft JDBC Driver 6.0, die „Immer verschlüsselt“ aktiviert:  
  
```  
String connectionString = "jdbc:sqlserver://localhost;user=<user>;password=<password>;columnEncryptionSetting=true;";  
  
```  
  
 „Immer verschlüsselt“ kann auch aktiviert werden, indem das Objekt SQLServerDataSource wie folgt verwendet wird:  
  
```  
SQLServerDataSource ds = new SQLServerDataSource(); ds.setColumnEncryptionSetting(true);  
  
```  
  
### Einfügen\/Abrufen von Daten \(Beispiel\)  
 Fügen Sie Daten in verschlüsselten Spalten ein, indem Sie SQLServerPreparedStatement\- oder SQLServerCallableStatement\-Objekte verwenden. Die Anwendung übergibt in den Set\-Methoden PreparedStatement oder CallableStatement nur Klartextwerte. Der Treiber verschlüsselt diese Werte dann transparent und übergibt die verschlüsselten Werte an den Server. Wenn verschlüsselte Spalten über ResultSet\-Objekte abgerufen werden, entschlüsselt der Treiber auf ähnliche Weise transparent die Werte, bevor er sie an die Anwendung sendet. Wenn eine Spalte verschlüsselt wird, sind für SQL Server keine Klartextdaten verfügbar. Er sendet\/empfängt nur verschlüsselte Daten.  
  
 So können Werte in verschlüsselte Spalten eingefügt bzw. aus diesen abgerufen werden:  
  
```  
import java.sql.*; import java.util.HashMap; import java.util.Map; import com.microsoft.sqlserver.jdbc.SQLServerColumnEncryptionJVMKeyStoreProvider; import com.microsoft.sqlserver.jdbc.SQLServerColumnEncryptionKeyStoreProvider; import com.microsoft.sqlserver.jdbc.SQLServerConnection; public class AlwaysEncrypted { // Name of the table private static String tblName = "Customers"; // Name of the column encryption key to be used for encryption. private static String columnEncryptionKey = "JDBC_CEK"; /** Specified details of the certificate to be used by Always Encrypted * User can choose from the following two options * 1. "Thumbprint:<Thumbprint of the certificate>" * 2. "Alias :<Alias of the certificate>" */ private static String key_Path_Thumbprint = "Thumbprint:ED1E941BC26D20BC7B42D03BB881EE5535CD0607"; /** *  Specifies the name of a key store provider , for JVM system provider use *  MSSQL_JVM_KEYSTORE */ private static String keyStoreProviderName = "MSSQL_JVM_KEYSTORE"; public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet objects that you create. // Open a sourceConnection to the database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { /** * Query to create table with Always Encrypted feature * For details on the systax please refer : https://msdn.microsoft.com/en-US/library/ms174979.aspx */ String createTblSQL = "CREATE TABLE " + tblName + " ( " + " FIRST_NAME varchar(100) COLLATE Latin1_General_BIN2 ENCRYPTED WITH (ENCRYPTION_TYPE = DETERMINISTIC,ALGORITHM = 'AEAD_AES_256_CBC_HMAC_SHA_256', COLUMN_ENCRYPTION_KEY = "+ columnEncryptionKey +" ) NOT NULL," + " LAST_NAME varchar(100) COLLATE Latin1_General_BIN2 ENCRYPTED WITH (ENCRYPTION_TYPE = DETERMINISTIC,ALGORITHM = 'AEAD_AES_256_CBC_HMAC_SHA_256', COLUMN_ENCRYPTION_KEY =  "+ columnEncryptionKey +" ) NOT NULL," + " SSN int ENCRYPTED WITH (ENCRYPTION_TYPE = DETERMINISTIC,ALGORITHM = 'AEAD_AES_256_CBC_HMAC_SHA_256', COLUMN_ENCRYPTION_KEY = " + columnEncryptionKey + " ) NOT NULL" + " ) "; try (Statement createTblStatement = sourceConnection.createStatement()) { // to create table createTblStatement.executeUpdate(createTblSQL); System.out.println("Table created with name : " + tblName); } // This map contains certificates and passwords Map<String, char[]> certPwds = new HashMap<String, char[]>(); // Thumbprint/Alias of certificate and password of associated private key certPwds.put(key_Path_Thumbprint, "password".toCharArray()); /** * Following arguments needed by  SQLServerColumnEncryptionJVMKeyStoreProvider * 1) keyStoreProviderName : Path where keystore is located. If null is provided default cacerts keystore is used * 2) keyStorePassword : Password of the keystore. * 3) Map<String,char[]> : Map of the certificate identifiers like thumbprint/alias and password for the corresponding private key */ SQLServerColumnEncryptionKeyStoreProvider storeProvider = new SQLServerColumnEncryptionJVMKeyStoreProvider( null, "password".toCharArray(), certPwds); // Map of all the key store provider names and handle to those providers Map<String, SQLServerColumnEncryptionKeyStoreProvider> providerMap = new HashMap<String, SQLServerColumnEncryptionKeyStoreProvider>(); providerMap.put(keyStoreProviderName, storeProvider); // registration of all the key store providers SQLServerConnection.registerColumnEncryptionKeyStoreProviders(providerMap); // inserting records in table String insertRecord="INSERT INTO " + tblName + " values (?,?,?)"; try (PreparedStatement insertStatement = sourceConnection.prepareStatement(insertRecord)) { insertStatement.setString(1, "First Name"); insertStatement.setString(2, "Last Name"); insertStatement.setInt(3, 1); insertStatement.executeUpdate(); System.out.println("Record inserted."); } // Selecting records from the table // Note: To filter data based on encrypted column values, use PreparedStatement paramters. String selectRecord="Select * from " + tblName; try (PreparedStatement selectStatement = sourceConnection.prepareStatement(selectRecord)) { ResultSet rs = selectStatement.executeQuery(); System.out.println("Getting records from the database."); while(rs.next()) { System.out.println("First name of customer : " + rs.getString("FIRST_NAME")); System.out.println("Last name of customer : " + rs.getString("LAST_NAME")); System.out.println("SSN of customer : " + rs.getInt("SSN")); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=ae;user=sa;password=****;columnEncryptionSetting=true"; return connectionUrl; } }  
  
```  
  
> [!NOTE]  
>  Die Vorschauversion von Microsoft JDBC Driver 6.0 verfügt über eine beschränkte Unterstützung für „Immer verschlüsselt“ mit gespeicherten Prozeduren, die mithilfe von CallableStatement ausgeführt werden. INPUT\-Parameter, die an eine gespeicherte Prozedur weitergegeben wurden, werden transparent verschlüsselt. Werte, die aus einem ResultSet\-Objekt in der Prozedur kommen, können ebenfalls transparent entschlüsselt werden. Die Vorschauversion unterstützt jedoch keine OUTPUT\-Parameter oder RETURN\-Werte für verschlüsselte Spalten.  
  
> [!NOTE]  
>  Abfragen können auf Spalten Übereinstimmungsvergleiche ausführen, wenn sie mittels deterministischer Verschlüsselung verschlüsselt sind. Weitere Informationen finden Sie im Abschnitt **Deterministische oder zufällige Verschlüsselung auswählen** des Themas [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
### Erstellen eines benutzerdefinierten CMK\-Speicheranbieters  
 Folgendes gehört zu den Informationen, die der Treiber von SQL\-Server für Abfrageparameter erhält, die verschlüsselt werden müssen, und für Abfrageergebnisse, die entschlüsselt werden müssen:  
  
-   Ein verschlüsselter Wert eines Spaltenverschlüsselungsschlüssels, der zum Ver\- oder Entschlüsseln eines Parameters oder Ergebnisses verwendet werden sollte.  
  
-   Der Name eines Schlüsselspeicheranbieters, der einen Schlüsselspeicher mit dem CMK kapselt, der zur Verschlüsselung des CEK verwendet wurde.  
  
-   Ein Schlüsselpfad, der den Speicherort des CMK im Schlüsselspeicher angibt.  
  
-   Der Name des Algorithmus, der verwendet wurde, um den CEK zu verschlüsseln.  
  
 Der Treiber verwendet die oben genannten Informationen, um die Implementierung des Schlüsselspeicheranbieters zur Entschlüsselung des abgerufenen CEK\-Werts zu verwenden. Anschließend wird dieser dann verwendet, um entweder einen Abfrageparameter zu verschlüsseln oder ein Abfrageergebnis zu entschlüsseln.  
  
 Der Treiber verfügt über eine Implementierung für einen Systemanbieter, SQLServerColumnEncryptionJVMKeyStoreProvider, der zum Speichern von CMKs in JVM Key Store verwendet werden kann.  
  
 Sie können einen benutzerdefinierte Schlüsselspeicheranbieter auch verwenden, indem Sie die SQLServerColumnEncryptionKeyStoreProvider\-Klasse erweitern und mithilfe der SQLServerConnection.registerColumnEncryptionKeyStoreProviders\(\)\-Methode registrieren. Weitere Informationen finden Sie im folgenden Beispiel:  
  
```  
public class MyCustomKeyStore extends SQLServerColumnEncryptionKeyStoreProvider{ public byte[] encryptColumnEncryptionKey(String masterKeyPath, String encryptionAlgorithm, byte[] plainTextColumnEncryptionKey) { // Code for encrypting the CEK } public byte[] decryptColumnEncryptionKey(String masterKeyPath, String encryptionAlgorithm, byte[] encryptedColumnEncryptionKey) { // Code for decrypting the CEK } }  
  
```  
  
 Registrieren Sie den Anbieter:  
  
```  
SQLServerColumnEncryptionKeyStoreProvider storeProvider = new MyCustomKeyStore(); Map<String, SQLServerColumnEncryptionKeyStoreProvider> keyStoreMap = new HashMap<String, SQLServerColumnEncryptionKeyStoreProvider>(); keyStoreMap.put("MY_CUSTOM_KEYSTORE", storeProvider); SQLServerConnection.registerColumnEncryptionKeyStoreProviders(keyStoreMap);  
  
```  
  
 Jeder in einem Schlüsselspeicher gespeicherte CMK muss in der Datenbank definiert werden. Verwenden Sie dazu [CREATE COLUMN MASTER KEY \(Transact\-SQL\)](https://msdn.microsoft.com/en-us/library/mt146393.aspx). Der Name des Schlüsselspeicheranbieters in der Definition des CMK muss mit dem Anbieternamen übereinstimmen, der in der Clientanwendung registriert ist.  Eine CMK\-Definition für diesen benutzerdefinierten Anbieter würde folgendermaßen aussehen:  
  
```  
CREATE COLUMN MASTER KEY [MyCustomCMK] WITH ( KEY_STORE_PROVIDER_NAME = N'MY_CUSTOM_KEYSTORE', KEY_PATH = N'<My_Custom_Path>' )  
  
```  
  
 Der CEK muss durch Aufrufen der Methode MyCustomKeyStore.encryptColumnEncryptionKey\(\) verschlüsselt werden. Erstellen Sie ihn darauf in der Datenbank mithilfe des Befehls CREATE COLUMN ENCRYPTION KEY T\-SQL. Alle mit diesem CEK verschlüsselten Spalten verwenden nun den benutzerdefinierten Schlüsselspeicheranbieter, um den CMK abzurufen.  
  
### „Immer verschlüsselt“ – API\-Referenz  
 Für Clientanwendungen, die „Immer verschlüsselt“ verwenden, sind mehrere neue Erweiterungen und Änderungen der JDBC\-Treiber\-API verfügbar.  
  
> [!NOTE]  
>  Diese Updates sind in Microsoft JDBC Driver 6.0 \(Vorschau\) für SQL Server verfügbar.  
  
 **SQLServerConnection\-Klasse**  
  
|Name|Beschreibung|  
|----------|------------------|  
|Neues Verbindungszeichenfolgen\-Schlüsselwort:<br /><br /> columnEncryptionSetting|columnEncryptionSetting\=true aktiviert die „Immer verschlüsselt“\-Funktionalität für die Verbindung und columnEncryptionSetting\=false deaktiviert sie. Zulässige Werte sind true oder false. Der Standardwert ist false.|  
|Neue Methode:<br /><br /> setColumnEncryptionTrustedMasterKeyPaths\(Map\<String, List\<String\>\> trustedKeyPaths\)|Ermöglicht Ihnen, eine Liste von vertrauenswürdigen Schlüsselpfaden für einen Datenbankserver festzulegen. Wenn der Treiber während der Verarbeitung eine Anwendungsabfrage einen Schlüsselpfad erhält, der nicht in der Liste enthalten ist, schlägt die Abfrage fehl. Diese Eigenschaft bietet zusätzlichen Schutz vor Angriffen, bei denen ein kompromittierter SQL Server gefälschte Schlüsselpfade bereitstellt, was zu Verlusten von Schlüsselspeicher\-Anmeldeinformationen führen kann.|  
|Neue Methode:<br /><br /> public Map\<String, List\<String\>\> getColumnEncryptionTrustedMasterKeyPaths\(\)|Gibt eine Liste von vertrauenswürdigen Schlüsselpfaden für einen Datenbankserver zurück.|  
|Neue Methode:<br /><br /> public void registerColumnEncryptionKeyStoreProviders \(Map\<String, SQLServerColumnEncryptionKeyStoreProvider\> clientKeyStoreProviders\)|Ermöglicht Ihnen, benutzerdefinierte Schlüsselspeicheranbieter zu registrieren. Dies ist ein Wörterbuch, das Anbieternamen von Schlüsselspeichern Implementierungen von Schlüsselspeicheranbietern zuordnet.<br /><br /> Um JVM Key Store zu verwenden, müssen Sie ein JSQLServerColumnEncryptionJVMKeyStoreProvider\-Objekt mit Anmeldeinformationen von JVM Key Store instanziieren und beim Treiber registrieren. Der Name für diesen Anbieter sollte „MSSQL\_JVM\_KEYSTORE“ sein.|  
  
 **SQLServerDataSource\-Klasse**  
  
|Name|Beschreibung|  
|----------|------------------|  
|Neue Methode:<br /><br /> public void setColumnEncryptionSetting\(boolean columnEncryptionSetting\)|Aktiviert\/deaktiviert die „Immer verschlüsselt“\-Funktionalität für das Datenquellenobjekt.<br /><br /> Der Standardwert ist deaktiviert.|  
|Neue Methode:<br /><br /> public boolean  getColumnEncryptionSetting\(\)|Ruft die „Immer verschlüsselt“\-Funktionalitätseinstellung für das Datenquellenobjekt ab.|  
  
 **SQLServerColumnEncryptionJVMKeyStoreProvider\-Klasse**  
  
 Die Implementierung der Schlüsselspeicheranbieters für JVM Key Store. Diese Klasse ermöglicht die Verwendung von Zertifikaten, die als CMKs in JVM Key Store gespeichert wurden.  
  
 Konstruktoren  
  
|Name|Beschreibung|  
|----------|------------------|  
|public SQLServerColumnEncryptionJVMKeyStoreProvider\(String keyStorePath, char\[\] keyStorePwd, Map\<String, char\[\]\> certPwds\)|Schlüsselspeicheranbieter für JVM Key Store.|  
  
 Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|public byte\[\] decryptColumnEncryptionKey\(String masterKeyPath, String encryptionAlgorithm, byte\[\] encryptedColumnEncryptionKey\)|Entschlüsselt den angegebenen verschlüsselten Wert eines CEK. Es wird erwartet, dass der verschlüsselte Wert verschlüsselt wird, indem das Zertifikat mit dem angegebenen Schlüsselpfad sowie der angegebene Algorithmus verwendet wird. Das Format des Schlüsselpfads sollte eines der folgenden sein:<br /><br /> -   Fingerabdruck: \<certificate\_thumbprint\><br />-   Alias:\<certificate\_alias\><br /><br /> \(Überschreibt SQLServerColumnEncryptionKeyStoreProvider.decryptColumnEncryptionKey \(String, String, Byte\[\]\).\)|  
|public byte\[\] decryptColumnEncryptionKey\(String masterKeyPath, String encryptionAlgorithm, byte\[\] encryptedColumnEncryptionKey\)|Verschlüsselt einen CEK, indem das Zertifikat mit dem angegebenen Schlüsselpfad und der angegebene Algorithmus verwendet wird. Das Format des Schlüsselpfads sollte eines der folgenden sein:<br /><br /> -   Fingerabdruck: \<certificate\_thumbprint\><br />-   Alias:\<certificate\_alias\><br /><br /> \(Überschreibt SQLServerColumnEncryptionKeyStoreProvider.encryptColumnEncryptionKey\(String, String, Byte\[\]\).\)|  
  
 **SSQLServerColumnEncryptionKeyStoreProvider\-Klasse**  
  
 Erweitern Sie diese Klasse, um einen benutzerdefinierten Schlüsselspeicheranbieter zu implementieren.  
  
|Name|Beschreibung|  
|----------|------------------|  
|SQLServerColumnEncryptionKeyStoreProvider|Basisklasse für alle Schlüsselspeicheranbieter. Ein benutzerdefinierter Anbieter muss von dieser Klasse abgeleitet werden, seine Memberfunktionen überschreiben und dann mithilfe von SQLServerConnection.registerColumnEncryptionKeyStoreProviders\(\) registriert werden.|  
  
 Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|public abstract byte\[\] decryptColumnEncryptionKey \(String masterKeyPath, String encryptionAlgorithm, byte \[\] encryptedColumnEncryptionKey\)|Basisklassenmethode, um den angegebenen verschlüsselten Wert eines CEK zu entschlüsseln. Es wird erwartet, dass der verschlüsselte Wert verschlüsselt wird, indem das Zertifikat mit dem angegebenen Schlüsselpfad sowie der angegebene Algorithmus verwendet wird.|  
|public abstract byte\[\] encryptColumnEncryptionKey \(String masterKeyPath, String encryptionAlgorithm, byte\[\]  columnEncryptionKey\)|Basisklassenmethode, um einen CEK mithilfe eines CMK mit dem angegebenen Schlüsselpfad und mithilfe des angegebenen Algorithmus zu verschlüsseln.|  
  
## Siehe auch  
 [„Immer verschlüsselt“ \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx)  
  
  