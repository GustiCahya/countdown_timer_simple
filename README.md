## CountdownTimer
A simple flutter countdown timer component.

## Installing
Add this to your package's pubspec.yaml file:
```yaml
dependencies:
  countdown_timer_simple: ^1.0.1
```
Install it
```yaml
$ flutter pub get
```
## Fields
| name                       | description                                                                                                                                                            |
| ---------------------- | ---------------------------------------------------- |
| endTime                | Countdown end time stamp                             |
| onEnd                  | Countdown end event                                  |
| emptyWidget            | The widget displayed at the end of the countdown     |
| defaultDays            | String defaultDays                                   |
| defaultHours           | String defaultHours                                  |
| defaultMin             | String defaultMin                                    |
| defaultSec             | final String defaultSec                              |
| daysSymbol             | final String daysSymbol                              |
| hoursSymbol            | final String hoursSymbol                             |
| minSymbol              | final String minSymbol                               |
| secSymbol              | final String secSymbol                               |
| textStyle              | final TextStyle textStyle                            |
| daysTextStyle          | final TextStyle daysTextStyle                        |
| hoursTextStyle         | final TextStyle hoursTextStyle                       |
| minTextStyle           | final TextStyle minTextStyle                         |
| secTextStyle           | final TextStyle secTextStyle                         |
| daysSymbolTextStyle    | final TextStyle daysSymbolTextStyle                  |
| hoursSymbolTextStyle   | final TextStyle hoursSymbolTextStyle                 |
| minSymbolTextStyle     | final TextStyle minSymbolTextStyle                   |
| secSymbolTextStyle     | final TextStyle secSymbolTextStyle                   |
| showDay                | final bool showDay                                   |
| showHour               | final bool showHour                                  |
| showMin                | final bool showMin                                   |
| ShowSec                | final bool showSec                                   |


## Example
Now in your Dart code, you can use:
```dart
import 'package:countdown_timer_simple/countdown_timer_simple.dart';

  ...
  int endTime = DateTime.now().millisecondsSinceEpoch + 1000 * 60 * 60;
  ...

  CountdownTimerSimple(endTime: endTime),
  CountdownTimerSimple(endTime: endTime,
    onEnd: (){
    print("Your time is up!");
    },
  ),
  CountdownTimerSimple(
    endTime: endTime,
    textStyle: TextStyle(fontSize: 30, color: Colors.orange),
  ),
  CountdownTimerSimple(
    endTime: endTime,
    defaultDays: "==",
    defaultHours: "--",
    defaultMin: "**",
    defaultSec: "++",
    daysSymbol: "days",
    hoursSymbol: "hour ",
    minSymbol: "minute ",
    secSymbol: "sec",
    daysTextStyle: TextStyle(fontSize: 20, color: Colors.red),
    hoursTextStyle:
        TextStyle(fontSize: 30, color: Colors.orange),
    minTextStyle:
        TextStyle(fontSize: 40, color: Colors.lightBlue),
    secTextStyle: TextStyle(fontSize: 50, color: Colors.pink),
    daysSymbolTextStyle:
        TextStyle(fontSize: 25, color: Colors.green),
    hoursSymbolTextStyle:
        TextStyle(fontSize: 35, color: Colors.amberAccent),
    minSymbolTextStyle:
        TextStyle(fontSize: 45, color: Colors.black),
    secSymbolTextStyle:
        TextStyle(fontSize: 55, color: Colors.deepOrange),
```

onEnd => End of time trigger

example 01
```
CountdownTimerSimple(endTime: DateTime.now().millisecondsSinceEpoch + 1000 * 60 * 60); // timestamp
```

example 02: Only display hours and seconds
```
CountdownTimerSimple(
    endTime: DateTime.now().millisecondsSinceEpoch + 1000 * 60 * 60,
    showDay = false,
    showHour = fales,
    onEnd: () {
        print("Your time is up!");
    }    
),
```
