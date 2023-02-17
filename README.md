In order to install React-Native framework, first create container with the Node.js stack. 
Node.js has it's own package manager `npm` with which you will install the Expo CLI.

Install the Expo CLI.
```Shell
npm install -g expo-cli
```

Now that you have the Expo CLI installed, init new expo project:
```Shell
expo init AwesomeProject
```

After the project is created, go to the project directory:
```Shell
cd AwesomeProject
```

To run React-Native application on a port run:
```Shell
RCT_METRO_PORT=3000 WEB_PORT=3001 expo start --web --tunnel
```




Install Tests

```Shell
npx expo install jest-expo jest
```

add following to `package.json`
```json
{		
	"scripts": {
		"test": "jest"
	},
	"jest": {
		"preset": "jest-expo",
		"transformIgnorePatterns": [
		"node_modules/(?!((jest-)?react-native|@react-native(-community)?)|expo(nent)?|@expo(nent)?/.*|@expo-google-fonts/.*|react-navigation|@react-navigation/.*|@unimodules/.*|unimodules|sentry-expo|native-base|react-native-svg)"
		]
	}
}
```
