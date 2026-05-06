# Property Tests

The checks below are meant to catch boring regressions before they become design debates.

The score rule for this repository weighs signal by 3, slack by 2, confidence by 2, and drag by 2. The important properties are monotonic signal, drag penalty, threshold consistency, and fixture id stability.

Run `powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1` from the repository root.
