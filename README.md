# Word Analyzer

import React, {Component} from 'react;
import {View, TextInput, Text, Alert} from 'react-native';

export default class App extends Component{
    constructor(props){
        super();
        this.state = {
            Words : [''],
            Consonents : 0,
            Vowels : 0, 
            Characters : 0
        };
    }

updateWords(){
    this.setState({Words : String.split})
}   

updateVowels(){
    if ( Vowels == 'a' || Vowels == 'e' || Vowels == 'i' 
    || Vowels == 'o' || Vowels == 'u') {
        this.setState ({Vowels : this.state.Vowels +1})
    }
}

updateConsonents(){
    if (Consonents >= 'a' && Consonents <= 'z') {
        this.setState ({Consonents : this.state.Consonents +1})
    }
}

updateCharacters(){
    this.setState({Characters : String.length})
}

render(){
    return(
        <View>
        <TextInput placeHolder = "Words" onChangeText={(Words) =>
        this.setState({Words})}/>
        <Text onPress = {() => this.updateWords()}>Analyze</Text>
        <Text> {this.state.value}</Text>
        </View>
    )
}
}
