# Mathnote FJS fork

This package is based on the published `fjs` 3.0.0 source and keeps its
Flutter Rust Bridge 2.12.0 generated API/runtime pair. The application pins
FRB 2.12.0 in `pubspec.yaml` because the 3.3.0 package release was generated
against a different FRB runtime.

Mathnote-specific changes for Phase 5 add deadline interruption and
request-scoped cancellation to the QuickJS-backed asynchronous runtime.
Regenerate bridge files with the pinned `flutter_rust_bridge_codegen` 2.12.0
and build/test the Linux native library before changing either version pin.

The copied source intentionally omits `libfjs/target` build output and the
upstream example app. Platform packaging files and Darwin frameworks remain
from the 3.0.0 release.
