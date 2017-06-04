# replace-html-placeholders
## Replacing the placeholders in html with their corresponding values from properties file
## 1) go to directory in unix :cd /var/tmp
cd /var/tmp

## 2) winscp the .tar.gz file to folder /var/tmp
## naveen_replacetokens.tar.gz

## 3) unzip the file using the below command
tar xvzf naveen_replacetokens.tar.gz -C /var/tmp

## it will create the folder 'naveen' which is having subfolders (input, conf, scripts, output)
## 4) go the folder  
cd /var/tmp/naveen/scripts

## 5) change the permissions of the files 
chmod -R 755 /var/tmp/naveen

## 6) execute the below command from the directory "cd /var/tmp/naveen/scripts"
## <<PROD ENVIRONMENT>>
./replaceTokens.sh ../input/index.html ../conf/prod.properties ../output/index_prod.html

## <<TEST ENVIRONMENT>>
./replaceTokens.sh ../input/index.html ../conf/test.properties ../output/index_test.html
