/**
 * @format
 */
import {AppRegistry} from 'react-native';
import {name as appName} from './app.json';
import WelcomeScreens from './screens/WelcomeScreens';
let fakeProducts = [
    {
        productname: 'Iphone 3',
        year: '2013'
    },
    {
        productname : 'Iphone 4',
        year: '2015'
    },
    {
        productname : 'Iphone 5',
        year: '2017'
    }
]
AppRegistry.registerComponent(appName, 
    () => () => <WelcomeScreens
                x = {5} y = {10}
                person = {{name: 'Nguyen Van Nghia',
                            age: '31',
                            email: 'nghianv2210bn@gmail.com'
                }}
                product = {fakeProducts}
                />)

import React from 'react';
import {Text, View} from 'react-native';
//
const WelcomeScreens = (props) =>{
//Destructuring an object
const {x, y} = props
const {person} = props
//const => let => var
//destrucuring person object
const {name, age, email} = person
const {products} = props
return <View style={{

}}>
     <Text>Value of x ={x}, Value of y ={y}</Text>
     <Text>name = {name}, email = {email}, age = {age}</Text>
    </View>
}
export default WelcomeScreens
