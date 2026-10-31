# QingPing (清屏)

[简体中文](README.md) | **English**

QingPing is an Android Accessibility-based assistant. Its goal is to reduce interference from splash-screen ads and accidental taps that trigger external app launches, and to record interception activity for target apps.

<p align="center">
  <a href="https://afdian.com/a/123xiaole">
    <img src="https://img.shields.io/badge/Afdian-Support%20the%20author-946CE6?style=for-the-badge" alt="Sponsor on Afdian">
  </a>
</p>
<p align="center"><strong>Voluntarily support project maintenance</strong> · <a href="SPONSOR.en.md">Sponsorship details</a> · <a href="SPONSOR.md">简体中文</a></p>

## Project Documents

- [Project issue records overview](docs/project-issues/README.md)
- [QingPing issue history and remaining items](docs/project-issues/问题记录.md)
- [Source code distribution and stripping notice](docs/SOURCE_DISTRIBUTION_NOTICE.md) (included in the source package)

## Scope of the Currently Published Source

The currently organized source release is **1.7.0-clean-source**. It is based on the original 1.7.0 source code. The following components from the early prototype have been removed: the third-party ad-rule JSON importer, its import UI, compatibility-field parsing, package-name hash matching, and the corresponding rule-execution entry point.

QingPing's own built-in ad recognition, security-control validation, observation mode, OCR/AI diagnostics, logs, and statistics remain. Historical documents may refer to the early compatibility prototype; those references are development history and do not mean that the current source still provides that functionality.

For the detailed removal list, retained functionality, and verification boundaries, see `SOURCE_DISTRIBUTION_NOTICE.md` in the source package.

## Security Principles

AI cannot directly authorize clicks. The word “Skip” appearing in body text or a title must not trigger ad skipping. Observation mode records results without clicking.

Screenshots captured by the automatic-recognition path are handled as short-lived in-memory objects and are not intended to be written to shared storage or uploaded. Images imported through the manual annotation tool are persistently stored in app-private storage as required by that feature. User-exported dataset ZIP files may be saved outside the app sandbox. These distinct data flows must not be conflated; it would be inaccurate to claim that **all** screenshots are never written to disk.

## Risk Boundaries

Removing the third-party rule compatibility layer is an engineering measure for source provenance management and reducing coupling; it is not a legal safe harbor. Code, rule data, trademarks, promotional statements, and actual operational conduct may raise different legal issues. Before public distribution or commercialization, seek review from a lawyer familiar with Chinese intellectual-property and competition law.
