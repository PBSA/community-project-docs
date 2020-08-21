# Setting up the Explorer

1\) clone the repo: `git clone git@github.com:peerplays-network/Block-Exporter.git`  
\(2\) cd into repo + npm i  
\(3\) switch to security-fixes branch  
\(4\) open server/config/main.js and replace `const BLOCKCHAIN_URL = 'wss://charlie.peerplays.download/api';`  
\(5\) open server/database/constants.js and replace with  


```text
module.exports = Object.freeze({
	HOST: '235.183.220.159',
	USER: 'pbsa',
	PASSWORD: 'password',
	DATABASE: 'explorer',
	RESTRICTED: ['temp-account', 'committee-account', 'null-account', 'proxy-to-self', 'relaxed-committee-account', 'test-dividend-distribution', 'witness-account'],
});
```

\(6\) Make sure vpn is on  
\(7\) `npm start` - starts application, you can proceed to `localhost:5000` and view it

