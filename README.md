# Flutter slider drawer

[![pub package](https://img.shields.io/pub/v/flutter_slider_drawer)](https://pub.dev/packages/flutter_slider_drawer)

A Flutter package with custom implementation of the Sider Drawer Menu

![Plugin example demo](demo.gif)




To start using this package, add `flutter_slider_drawer` dependency to your `pubspec.yaml`

```yaml
dependencies:
  flutter_slider_drawer: '<latest_release>'
```

 

# Features

  - Slider with custom animation time
  - Provide Basic Appbar with customization of color, sizes and title
  - Dynamic slider open and close offset
  - Provide drawer icon animation 

# Code 

```
SliderMenuContainer(
            appBarColor: Colors.white,
            key: _key,
            appBarPadding: const EdgeInsets.only(top: 20),
            sliderMenuOpenOffset: 250,
            appBarHeight: 60,
            title: Text(
              title,
              style: TextStyle(fontSize: 22, fontWeight: FontWeight.w700),
            ),
            sliderMenuWidget: MenuWidget(
              onItemClick: (title) {
                _key.currentState.closeDrawer();
                setState(() {
                  this.title = title;
                });
              },
            ),
            sliderMainWidget: MainWidget()),
 ```
 
 
### Controlling the drawer

```
GlobalKey<SliderMenuContainerState> _key =
      new GlobalKey<SliderMenuContainerState>();
  
   @override
  Widget build(BuildContext context) {
  return SliderMenuContainer(
            appBarColor: Colors.white,
            key: _key,
            sliderMenuWidget: MenuWidget(
              onItemClick: (title) {
                _key.currentState.closeDrawer();
                setState(() {
                  this.title = title;
                });
              },
            ),
           sliderMainWidget: MainWidget()),
      ),
      
```

* Using the below methods for controll drawer.
``` 
 _key.currentState.closeDrawer();
 _key.currentState.openDrawer();
 _key.currentState.toggle();
 _key.currentState.isDrawerOpen();
 ```


