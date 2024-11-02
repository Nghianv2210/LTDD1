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
