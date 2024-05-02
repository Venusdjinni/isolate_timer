A simple timer logic running in an isolate. Built with BLoC.

## Getting started

This package provides a [BLoC](https://pub.dev/packages/bloc) cubit that manage a timer running inside an isolate.

## Usage

```dart
// creates a TimerCubit that will run from startTime to finishTime
final startTime = DateTime(2024, 11, 20, 10);
final finishTime = DateTime(2024, 11, 20, 10, 0, 50);
final timerCubit = TimerCubit(startTime, finishTime);

// creates a timer that will run from now and will last the given duration
final durationTimerCubit = TimerCubit.duration(Duration(minutes: 5));

// get the total duration of the timer
print(timerCubit.maxDuration);

// restarts the timer
timerCubit.reset();

// displays a duration in a mm:ss format
print(durationToMinutes(Duration(minutes: 3, seconds: 20))); // '03:20'
```

