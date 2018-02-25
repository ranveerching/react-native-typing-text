# react-native-typing-text

react-native-typing-text is a purely javascript based animated typing text plugin with blinking cursor support for react native applications.

### Installation
```
npm install react-native-typing-text --save
```
### Properties
```
text: "Default Typing Animated Text." // Text which will be displayed as typed text.
color: "rgb( 77, 192, 103 )" // Color of the text and blinking cursor.
textSize: 30 // Font size of text and blinking cursor.
typingAnimationDuration: 50 // Duration between previous and newly typed character.
blinkingCursorAnimationDuration: 190 // Duration of blinking animation for cursor.
```
### Screenshots
![alt text](https://3.bp.blogspot.com/-XX8i5ud7Yi8/WpJp1xMio5I/AAAAAAAAAtg/SyXA-jGG_kUIZgqqIzXV16UjldqVhwOhQCLcBGAs/s1600/typing-text.gif)
### Usage Example
* Generate a new react native project.
```
react-native init TypingText
cd TypingText
npm install react-native-typing-text --save
```
* Then paste the following code into your App.js file:
```
import React, { Component } from 'react';
import { StyleSheet, View } from 'react-native';
import TypingText from 'react-native-typing-text';

export default class App extends Component<{}>
{
    render()
    {
        return(
            <View style = { styles.container }>
                <TypingText
                    text = "The European languages are members of the same family. Their separate existence is a myth. For science, music, sport, etc, Europe uses the same vocabulary. The languages only differ in their grammar."
                />
            </View>
        );
    }
}

const styles = StyleSheet.create(
{
    container:
    {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        paddingHorizontal: 10,
        backgroundColor: 'black',
        paddingTop: ( Platform.OS === 'ios' ) ? 20 : 0
    }
});
```
