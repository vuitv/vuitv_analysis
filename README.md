# VuiTv Analysis

![flutter_version][flutter_badge]
[![style: vuitv analysis][badge]][badge_link]

A project create by VuiTv 🤖

---
## Usage

To use the lints, add as a dev dependency in your `pubspec.yaml`:

```yaml
dart pub add dev:vuitv_analysis
# or
flutter pub add dev:vuitv_analysis
```

Then, add an include in `analysis_options.yaml`:

```yaml
include: package:vuitv_analysis/analysis_options.yaml
```

This will ensure you always use the latest version of the lints. If you wish to restrict the lint version, specify a version of `analysis_options.yaml` instead:

```yaml
include: package:vuitv_analysis/analysis_options.3.7.0.yaml
```

## Suppressing Lints

There may be cases where specific lint rules are undesirable. Lint rules can be suppressed at the line, file, or project level.

An example use case for suppressing lint rules at the file level is suppressing the `prefer_const_constructors` in order to achieve 100% code coverage. This is due to the fact that const constructors are executed before the tests are run, resulting in no coverage collection.

### Line Level

To suppress a specific lint rule for a specific line of code, use an `ignore` comment directly above the line:

```dart
// ignore: public_member_api_docs
class A {}
```

### File Level

To suppress a specific lint rule of a specific file, use an `ignore_for_file` comment at the top of the file:

```dart
// ignore_for_file: public_member_api_docs

class A {}

class B {}
```

### Project Level

To suppress a specific lint rule for an entire project, modify `analysis_options.yaml`:

```yaml
include: package:vuitv_analysis/analysis_options.yaml
linter:
  rules:
    public_member_api_docs: false
```

## Badge

To indicate your project is using `vuitv_analysis` →
[![style: vuitv analysis][badge]][badge_link]

```md
[![style: vuitv analysis](https://img.shields.io/badge/style-vuitv_analysis-B22C89.svg)](https://pub.dev/packages/vuitv_analysis)
```

[flutter_badge]: https://img.shields.io/badge/pub-v3.7.0-blue
[badge]: https://img.shields.io/badge/style-vuitv_analysis-B22C89.svg
[badge_link]: https://pub.dev/packages/vuitv_analysis