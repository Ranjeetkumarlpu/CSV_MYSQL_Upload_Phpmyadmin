# CSV_MYSQL_Upload_Phpmyadmin

Upload Query :

ALTER TABLE `[insert table name]` DISABLE KEYS;
LOAD DATA INFILE '[insert full path to your csv here]' 
INTO TABLE 
`[insert table name]` 
CHARACTER SET UTF8 
FIELDS TERMINATED BY ','  
ENCLOSED BY '"' 
LINES TERMINATED BY '\n';
ALTER TABLE `[insert table name]` ENABLE KEYS;

or

ALTER TABLE `products` DISABLE KEYS;
LOAD DATA INFILE 'C:/Users/abc/Desktop/rk.csv' 
INTO TABLE 
`products` 
CHARACTER SET UTF8 
FIELDS TERMINATED BY ','  
ENCLOSED BY '"' 
LINES TERMINATED BY '\n';
ALTER TABLE `products` ENABLE KEYS;

PHP Upload : 

⋖?php
$filename = '[insert full path to your csv here]';
$file = new \SplFileObject($filename, 'r');
$file-⋗seek(PHP_INT_MAX);
$total_lines = $file-⋗key() + 1; 
unset($file);
$file = null;
echo '⋖h2⋗The File has '.number_format($total_lines).' Lines⋖/h2⋗';
?⋗

Large File CSV Upload : https://www.youtube.com/watch?v=6IByt5doavQ

Execution_time_Error Source : https://www.youtube.com/watch?v=7aFr3e9q9XQ

Source : https://phoenixnap.com/kb/import-csv-file-into-mysql

SQL : https://www.youtube.com/watch?v=-thOn1NKJew&list=PL_RGaFnxSHWr_6xTfF2FrIw-NAOo3iWMy

Create Table in mysql : https://www.youtube.com/watch?v=WNK1unCzpds

Import Excel File in MYSQL : https://www.youtube.com/watch?v=zE1qMRdgkKU&feature=youtu.be
