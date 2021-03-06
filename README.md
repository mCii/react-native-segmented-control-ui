# react-native-segmented-control-ui(for Android/iOS) 🚀

[![npm](https://img.shields.io/npm/v/react-native-segmented-control-ui.svg?style=flat-square "npm version")](https://www.npmjs.com/package/react-native-segmented-control-ui)
[![Monthly Downloads](https://img.shields.io/npm/dm/react-native-segmented-control-ui.svg?style=flat-square )](https://npmjs.org/package/react-native-segmented-control-ui)
[![Build Status](https://travis-ci.org/gbhasha/react-native-segmented-control-ui.svg?branch=master)](https://travis-ci.org/gbhasha/react-native-segmented-control-ui)
[![codecov](https://codecov.io/gh/gbhasha/react-native-segmented-control-ui/branch/master/graph/badge.svg)](https://codecov.io/gh/gbhasha/react-native-segmented-control-ui)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/079cec8db0c34a7fabe41011eab8483d)](https://www.codacy.com/app/gbhasha/react-native-segmented-control-ui?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=gbhasha/react-native-segmented-control-ui&amp;utm_campaign=Badge_Grade)

[![NPM](https://nodei.co/npm/react-native-segmented-control-ui.png?compact=true)](https://npmjs.org/package/react-native-segmented-control-ui)


An extendable tab components for React Native similar to iOSSegmentedControl, Primarily built to support both iOS and Android.



## Usage

```javascript
import SegmentedControlTab from 'react-native-segmented-control-ui'

const ConsumerComponent extends Component {

    constructor(){
        super()
        this.state = {
            selectedIndex: 0
        };
    }

    handleIndexChange = (index) => {
        this.setState({
            selectedIndex: index
        });
    }

    render() {
        return (
            <View>
                <SegmentedControlTab
                    values={['First', 'Second', 'Third']}
                    selectedIndex={this.state.selectedIndex}
                    onTabPress={this.handleIndexChange}
                    />
            </View>
        );
    }
}
```

## API

Name | Description | Default | Type
------|-------------|----------|-----------
values | titles of tabs  | `['One', 'Two', 'Three']` | array
selectedIndex | index of tab item to be selected initially| [0] | number
borderRadius | borderRadius of whole tab | 5 | number
tabsContainerStyle | external styles can be passed to override the default styles of the segmentedControl wrapper| [tabsContainerStyle](#custom-styling)  | object(styles)
tabStyle | external styles can be passed to override the default styles of the tabs| [tabStyle](#custom-styling)  | object(styles)
tabTextStyle | external styles can be passed to override the default styles of the tab title| [tabTextStyle](#custom-styling)  | object(styles)
activeTabStyle | external styles can be passed to override the default styles of the active tab| [activeTabStyle](#custom-styling)  | object(styles)
activeTabTextStyle | external styles can be passed to override the default styles of the active tab text| [activeTabTextStyle](#custom-styling)  | object(styles)
badges | badges values to display  | `[1, 2, 3]` | array
tabBadgeContainerStyle | external style can be passed to override the default style of the badge container | [tabBadgeContainerStyle](#custom-styling)  | object(styles)
activeTabBadgeContainerStyle | external style can be passed to override the default style of the active badge container | [activeTabBadgeContainerStyle](#custom-styling)  | object(styles)
tabBadgeStyle | external style can be passed to override the default style of the badge text | [tabsContainerStyle](#custom-styling)  | object(styles)
activeTabBadgeStyle | external style can be passed to override the default style of the active badge text | [activeTabBadgeStyle](#custom-styling)  | object(styles)
onTabPress | call-back function when a tab is selected | () => {} | func
allowFontScaling | whether the segment & badge text should allow font scaling (default matches React Native default) | true | bool
accessible | enables accessibility for each tab | true | bool
accessibilityLabels | Reads out the given text on each tab press when voice over is enabled. If not set, uses the text passed in as values in props as a fallback | ['Label 1', 'Label 2', 'Label 3'] | array
testIDs | Unique identifier for each tab which acts as a hook for functional test | ['Label 1', 'Label 2', 'Label 3'] | array


## Custom styling
    ```javascript
        <SegmentedControlTab
          tabsContainerStyle={styles.tabsContainerStyle}
          tabStyle={styles.tabStyle}
          tabTextStyle={styles.tabTextStyle}
          activeTabStyle={styles.activeTabStyle}
          activeTabTextStyle={styles.activeTabTextStyle}
          selectedIndex={1}
          allowFontScaling={false}
          values={['First', 'Second', 'Third']}
          onPress={this.handleIndexChange}
        />

        const styles = StyleSheet.create({
            tabsContainerStyle: {
            borderColor: '#706fd3'
        },
        tabStyle: {
            borderLeftColor: '#706fd3',
            backgroundColor: 'transparent',
        },
        activeTabStyle: {
            backgroundColor: '#33d9b2'
        },
        tabTextStyle: {
            color: '#706fd3'
        },
        })
    ```


## Try it out
You can try it out default example online using [`Expo Snack`](https://snack.expo.io/@gbhasha/example-of-react-native-segmented-control-ui)

You can try it out custom styling example online using [`Expo Snack`](https://snack.expo.io/@gbhasha/custom-styling-of-react-native-segmented-control-ui)

### Example

Look at the full example code at [`/Example`](/Example) folder to run the expo app locally. or try with Exponent App [here](https://expo.io/@gbhasha/react-native-segmented-control-ui).

## ScreenShots

### Android

![Demo](https://github.com/gbhasha/react-native-segmented-control-ui/blob/master/Example/screenshots/android-Nexus6p.png)

### iOS

![Demo](https://github.com/gbhasha/react-native-segmented-control-ui/blob/master/Example/screenshots/ios-iphone6.png)

## License
*MIT*
