# Encra: selected validation and evidence limits

[Back to the project overview](README.md)

This validation summary was initially prepared on November 7, 2026 from the private project's documentation and selected test-source inspection. No builds or tests were rerun for that initial documentation review. The November 1 results below remain historical project-record results.

Later on November 7, the app was built and selected simulator UI scenarios were run to capture the showcase's sample-data screenshots. Those capture runs did not repeat the historical validation summarized below and do not establish a full regression pass or independent security assessment. Internal reports, device identifiers, and test-fixture source remain private.

## What the tests exercise

| Area | Selected scenarios in the test suite |
| --- | --- |
| Vault identity | Creation and reuse of an authenticated identity; missing keys do not create replacements; tampered identity blocks operations. |
| Recovery archives | Exact metadata and multi-chunk content round trips; archive sizing and progress; checks for disclosure of fixture content, metadata, or recovery secrets. |
| Transfer authorization | Denial before root-key access; fresh approval for direct transfers; batch approval bound to its sources and destinations; cancellation, expiry, and late callbacks. |

These descriptions were checked against test source. A test's presence establishes intended coverage, not that it passed on every platform or detects every possible failure. Fixture-based confidentiality assertions do not prove general cryptographic security.

## Selected historical results

The private project's November 1, 2026 validation notes record:

- **202 unit tests passing**, comprising 261 executed cases including parameterized cases, with zero failures or skips, in an iPhone simulator run.
- **Four UI checks passing** in a separate run covering export-format and secret switching, encrypted import through app switching, backup preparation/discard, and backup verification through app switching.
- **Unsigned iOS and macOS Release builds passing.**
- **Signed iPhone and iPad deployment checks succeeding** for installation, launch, and installed-version queries.

The UI checks preceded a final archive key-revalidation adjustment; the recorded final unit run covered that adjustment. These are historical project-record results. Original result bundles were not independently reprocessed for this showcase, and these counts do not describe a fresh run of the current revision.

## What remains separate

- Actual Face ID and Touch ID failure, enrollment, lockout, and device-lock behavior across supported devices.
- Interrupted plaintext-export cleanup using physical devices and real system save/share panels.
- Broad hardware and operating-system compatibility, long-running use, and large-file export handoff under varied device conditions.
- Independent assessment of the security design and implementation, including malicious-media testing.

Simulator authentication uses controlled responses. Successful build, installation, and launch do not establish every runtime workflow or security property. Encra has not received an independent security assessment, and this portfolio does not claim one.
