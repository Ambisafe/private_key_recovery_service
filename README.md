# Ambisafe encrypted container decryption and private key recovery

This process was developed to make your wallet as safe as possible. It allows recovering private key from a backup of the encrypted container from wallets and ICOs powered by Ambisafe. You have to remember your account password that was used at the service you've got the backup from.

**Security notice: Ambisafe NEVER gets, stores or requests your decrypted data. 
All the decryption happens inside your web browser and the resulted key should NOT be shared with anybody!
If somebody asks you to perform the recovery - please contact the support immediately.
The contents of the container give full access to the coins/tokens/funds on your crypto wallet.
**

Follow the next steps to decrypt your wallet container:


1) Open the page from Github using https://rawgit.com/Ambisafe/private_key_recovery_service/master/src/index.html 

2) Copy the text of encrypted container which was emailed to you.
Please copy all the text as it’s shown in the example below.
Example:
```json
{
"public_key": "02f3ec6d3f8a79be1c2de1612e9dbf49a2dc9e9a198d7d6326964ebbe521947dd3", 
"data": "cec39e1493859f948fd99ff9debcb5e49eb3d347320b9f71660fd649b92575a973cafe6ef429c593ffc89293d1365f25", 
"salt": "f93b9730ac8e2c5c43073c5184b9182dbc97d3aa", 
"iv": "9f9855ea48703554b94410f1fe601112"
}
```

3) Paste the text of encrypted container (1) and your account password (2) at the HTML page (check the screenshot below):

<img src="/img/container_paste_helper.png"/>

4) Press "Decrypt" button, the result will be PrivateKey, PublicKey and address.

5) Save this decrypted data and **never share your decrypted private key with any third parties**. 
Keep in mind that the person who has access to your decrypted private key has full control over your assets.

6) The decrypted private key can be used in MyEtherWallet to control the assets on your address.


## How to check that the process is safe?

1a) Download this repository to your local computer by clicking button "Clone or download" > Download ZIP:
<img src="/img/download_help_pic.png"/> 

2) Extract repository archive on your computer and open the extracted folder.

3) In extracted folder open folder *src*

4) In the *src* folder find file *index.html* and open it with your web browser (Chrome is 100% compatible).

You can browse the Javascript and HTML sources that are used on this page to check the decryption algorithm. 
