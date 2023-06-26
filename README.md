Applicazione di Verifica One-Time Password (OTP)
Questa è una semplice applicazione web che illustra il processo di verifica della One-Time Password (OTP). L'applicazione è sviluppata utilizzando Flask, un framework web per Python, e consente agli utenti di effettuare l'accesso con le proprie credenziali e successivamente verificare la propria identità utilizzando una OTP generata casualmente e inviata all'indirizzo email dell'utente.

Come Funziona
L'utente accede all'applicazione attraverso la pagina iniziale ("/") e visualizza un modulo di accesso.
Dopo aver compilato il modulo di accesso, l'applicazione verifica le credenziali inserite (nome utente e password). Se le credenziali corrispondono ai valori predefiniti, l'applicazione procede generando una OTP e inviandola all'indirizzo email dell'utente.
La OTP viene generata utilizzando una stringa casuale di 6 cifre.
La OTP viene inviata all'indirizzo email dell'utente utilizzando il protocollo SMTP. In questo esempio, viene utilizzato un account Gmail per l'invio dell'email, ma è possibile configurare l'applicazione per utilizzare un diverso servizio email modificando la configurazione SMTP.
La OTP viene memorizzata temporaneamente nella memoria del server, associata al nome utente dell'utente.
L'utente viene reindirizzato a una pagina di verifica ("/verify_otp") in cui viene richiesto di inserire la OTP ricevuta tramite email.
Alla conferma della OTP, l'applicazione recupera la OTP memorizzata per l'utente e la confronta con quella inserita.
Se la OTP inserita corrisponde alla OTP memorizzata, viene visualizzata una pagina di accesso consentito ("access_granted.html").
