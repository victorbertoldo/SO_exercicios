#!/bin/bash
# mysqlBackup.sh
# Victor Bertoldo

DATA=`/bin/date +%Y%m%d`

# diretório de backup
NOME="/dev/sdb1/PRODUCAO-$DATA.sql"

# variáveis do MySQL
HOST="localhost"
ETL="10.0.0.1"
USER="sa"
PASSWORD="micr0XPo!"
PASSETL="bkp#03BV"
DATABASE1="PRODUCAO"
DATABASE2="PROD-BKP"

#geração da base d-1
mysqldump -h $HOST -u $USER -p$PASSWORD -D $DATABASE1 > $NOME

mysql -h $ETL -u $USER -p$PASSETL -D $DATABASE2 < $NOME

################## -- FIM -- ###########################

Salve o arquivo /DIRETORIO_EXEMPLO/EXEMPLO/mysqlBackup.sh
execute o comando:

#crontab -e
add a linha "0 2 * * * /bin/sh /DIRETORIO_EXEMPLO/EXEMPLO/mysqlBackup.sh"

Pronto!
