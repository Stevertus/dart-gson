# dart-gson

Parses and encodes the json generated by GSON (Can parse minecraft's json)

This is just a simple parser and decoder.

Website (github pages): [https://miniminelp.github.io/dart-gson/](https://miniminelp.github.io/dart-gson/)

Repository (github): [https://github.com/MinimineLP/dart-gson](https://github.com/MinimineLP/dart-gson)

View dart docs: [https://miniminelp.github.io/dart-gson/doc/api/gson/gson-library.html](https://pub.dev/documentation/gson/latest/)

View on pub: [https://pub.dev/packages/gson](https://pub.dev/packages/gson)

## Installation

Add this to your
`pubspec.yaml`
file

```yaml
dependencies:
  gson: ^0.1.2
```

And to import use

```dart
import 'package:gson/gson.dart';
```

## Usage

To decode you can use

```dart
gson.decode("{...}");
```

and to decode you can use

```dart
gson.encode({...});
```

As dart has no different variable types for numbers (there are just `num`, `int` and `double`), the api gives you types.
So if you want a double for example in the output you have to insert

```dart
gson.encode(new Double(1.0)); // >> 1.0d
```

Also the compiler gives these classes back to you, so you have to get the value property

```dart
gson.decode("1.0d").value; // >> 1.0
```

because booleans are displayed as bytes in gson, the boolean value is in the Byte type.

```dart
gson.encode(true) // >> 1b
gson.decode("1b").value // >> 1
gson.decode("1b").boolValue // >> true (and 0b will be false)
```

The program can't find the difference between the number 1 and true / the number 0 / false, because in the code it is the same.

For more examples see [example/example.dart](https://github.com/MinimineLP/dart-gson/blob/master/example/example.dart)

## License

BSD 2-Clause License (See [LICENSE](LICENSE))

## Issues

Please post issues [here](https://github.com/MinimineLP/dart-gson/issues)
