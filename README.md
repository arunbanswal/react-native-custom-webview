# react-native-custom-webview
I am just using the https://github.com/d-a-n/react-native-webbrowser to create a back button. Credit goes to 
https://github.com/d-a-n/react-native-webbrowser
https://github.com/magrinj/react-native-webbrowser

A cross-platform (iOS / Android), full-featured in-app web browser component for React Native that is highly customizable. Currently you can hide the address-, status- and toolbar. Additionally the foreground and background colors can be modified.
 
## Install

```sh
npm i react-native-custom-webview --save
```

## Usage

Here is an extensive overview of the component usage.

```jsx

class SampleApp extends Component {
    render() {
        const goBack = () => 
        {
            this.props.navigation.goBack()
        }
        return (
            <View style={{paddingTop:20, flex:1}}>
                <Webbrowser
                    url="https://facebook.github.io/react-native/docs/"
                    hideHomeButton={false}
                    hideToolbar={false}
                    hideAddressBar={false}
                    hideStatusBar={true}
                    backButtonVisible={true}
                    onBackPress= {() => {goBack()}}
                    foregroundColor="#D61B5D"
                    backgroundColor="#F3848A"
                />
                
            </View>
        );
    }
}
```

## Props

* `url - string` required, web address
* `hideAddressBar - bool` optional, hides the address bar / address input
* `hideStatusBar - bool` optional, hides the status bar / site title
* `hideToolbar - bool` optional, hides the toolbar (nav bar)
* `hideHomeButton - bool` optional, hides just the home button from the toolbar
* `hideActivityIndicator - bool`optional, hides the activity indicator (loading) overlay 
* `foregroundColor - string` optional, sets the forground color of text and icon elements
* `backgroundColor - string` optional, sets the background color
* `onNavigationStateChange - function(navState)` optional, url change callback
* `onShouldStartLoadWithRequest - function(event)` optional, return false if the request should be stopped


## Screenshots 
With Back button

<img src="https://raw.githubusercontent.com/squatto/react-native-custom-webview/master/assets/images/screenshot3.png" width="400" />
&nbsp;&nbsp;&nbsp;
<img src="https://raw.githubusercontent.com/squatto/react-native-custom-webview/master/assets/images/screenshot.png" width="400" />


