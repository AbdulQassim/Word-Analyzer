# Word Analyzer
import React, {Component} from 'react';
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
myLine = this.state.Words;
myLine = myline.toLowerCase();
myLine = myLine.split();

for(var i = 0; i < myline.length(); ++i ){
    var alphabet = myLine.charAt(i);
        if (alphabet == 'a' || alphabet == 'e' || alphabet == 'i' 
            || alphabet == 'o' || alphabet == 'u'){
                this.setState ({Vowels : this.state.Vowels +1});
            }
        else {
            this.setState ({Consonents : this.state.Consonents +1});
        }
}
}

render(){
   
    return(
        <View>
        <TextInput onChangeText={(Words) => this.setState({Words})} placeHolder = "Input a word"/>
        <Button onPress={this.updateWords} title='Analyze'/>
        <Text>Word: {this.state.Words}</Text>
        <Text>No of Vowels: {this.state.Vowels}</Text>
        <Text>No of Consonents: {this.tate.Consonents}</Text>
        <Text>No of Characters: {this.state.Characters}</Text>
        </View>
    );
}
}

/* Work division : Iqbal - function update work
                    Abidil - Constructor & jsx */
