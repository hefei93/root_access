[![pub package](https://img.shields.io/pub/v/root_access.svg)](https://pub.dartlang.org/packages/root_access)

# Root access Plugin
A Flutter plugin for getting root access in Android apps.

#### This plugin is based on [RootTools](https://github.com/Stericson/RootTools) by [Stericson](https://github.com/Stericson).

#### This plugin is only for Android platform. 

## Usage

### Import  the root_access plugin
Follow the [plugin installation instructions](https://pub.dartlang.org/packages/root_access#-installing-tab-).

### Use the plugin
```
import 'package:root_access/root_access.dart';
```

Define a bool variable and assign a value
```
bool _rootStatus = false;
```

The ```RootAccess``` class provides a getter to get root access and status
```
bool rootStatus = await RootAccess.rootAccess;
```

Declare an async method to retrieve root access
```
Future<void> initRootRequest() async {
    bool rootStatus = await RootAccess.rootAccess;
    setState(() {
      _rootStatus = rootStatus;
    });
  }
```

Later you can use ```_rootStatus``` in your code to let app know the status of root access.
If it's ```false``` then root access is not granted in access prompt dialog and if it's true then root access has been granted to the app.  
## Example

See the [example application](https://github.com/amitkhairnar44/root_access/tree/master/example) source
for a complete sample app using the Root Access plugin.

## Issues and feedback

Please file [issues](https://github.com/amitkhairnar44/root_access/issues/new)
to send feedback or report a bug. Thank you!