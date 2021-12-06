# Linux&Bash

1. Spiega in due parole cosa fa questo script bash:

  ```
    if [ -d $1 ]
    then
      DIR=$(pwd)
      TMP_FILE="$DIR/archive.tar"
      tar cvf $TMP_FILE $1
      scp $TMP_FILE root@somedomain.it:/tmp/
      rm $TMP_FILE
    else
      echo "Path is not a directory"
      exit
    fi
  ```

2. Eseguendo il precedente script viene richiesta la password di accesso per l'account root sulla macchina che risponde al dominio `somedomain.it`. Come si potrebbe mantenere la stessa funzionalità evitando la richiesta della password e di configurarla all'interno dello script (hai ovviamente accesso di root al server in questione)?

3. Immagina di avere un servizio chiamato `myservice` in esecuzione. Scrivi uno script in bash per killare il suo processo.

4. Dove risiedono solitamente i file di configurazione dei vari applicativi?

5. Cosa fa il comando seguente, e a cosa potrebbe servire?

  ```
    crontab -e
  ```
