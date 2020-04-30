# REACT CODE SNIPPETS
# Create REACT APP
```
npx create-react-app my-app
cd my-app
npm start
```
# Fetch data from API REACT
``` REACT JS
import React, {Component} from 'react'

export default class StarWars extends Component {
    constructor(){
        super()
        this.state = {
            character: {},
            isLoading: false
        }
    }

    componentDidMount(){
        this.setState({isLoading: true})
        fetch("https://swapi.co/api/people/1")
            .then(response => response.json())
            .then(data => (
                this.setState({
                    isLoading: false,
                    character: data
                })
            ))
    }

    
    render(){
        const text = this.state.isLoading ? "People data is loading..." : this.state.character.name
        return(
            <div>
                <p>{text}</p>
            </div>
        )
    }
}
```
# ROUTING
```
ReactDOM.render(( 

  <Switch> 

    <Route exact path="/" component={Home} /> 

    <Route path="/login" component={Login} /> 

    <Route path="/explore" component={Explore} /> 

  </Switch>), 

  document.getElementById('root') 

); 
```
# Update REACT Dependancies or Libraries
```
npm install -g npm-check-updates 
ncu -u 
npm update 
npm install
```
# npm run build
```
Builds the app for production to the build folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.

Your app is ready to be deployed.
```
