name: Flutter CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - uses: subosito/flutter-action@v2
      with:
        flutter-version: 'latest'
    - run: flutter pub get
    - run: flutter analyze
    - run: flutter test
# shop-ease
Flutter tabanlı yenilikçi alışveriş uygulaması.
