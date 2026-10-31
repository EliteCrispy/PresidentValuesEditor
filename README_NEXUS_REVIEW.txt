PRESIDENT VALUES EDITOR v0.1.1 - SOURCE REVIEW PACKAGE

PURPOSE
-------
This is source and supporting material for review of the President Values
Editor v0.1.1 release. It is not an installable mod package. The installed
runtime Payload, compiled editor plugin and gameplay screenshot are omitted.
Do not run Install_Editor.cmd from this source-review package; its required
Payload is intentionally absent. The helpers are included for inspection.

Nexus mod page:
https://www.nexusmods.com/mods/1?game_id=10883

Providing source for inspection does not establish Nexus approval or identify
the cause of a quarantine warning. No approval or false-positive finding is
claimed by this package.

ORIGINAL RELEASE IDENTIFICATION
------------------------------
Original public/quarantined file: PresidentValuesEditor_v0.1.1.zip
Original ZIP size: 46,121,623 bytes
Original ZIP SHA-256:
7ACF1C812692DEAABC962C56D1E13485C1BA8A57B530F7AD1A9F399FA842FA04

Tested editor: PresidentValuesEditor.dll, v0.1.1, 33,280 bytes
Tested editor SHA-256:
DDE1D64AA6A25D4C5A42D2108ED97FB7ECE8B25C2818937E94E66686C5EE2E9B

Supported game: President Simulator by Studio 14b, Steam app 3705900,
build 26325310, Unity 6000.3.9f1, Windows x64. The public release and its
tested plugin have not been modified to prepare this review package.

CONTENTS AND REVIEW STARTING POINTS
---------------------------------
Source/Editor/src/PresidentValuesEditor/
  The original v0.1.1 C# editor source and project file.
Source/Editor/tests/Rules.Tests/
  Numeric/state-transition test source; these tests need no game references.
Installer.Common.ps1, Manage_Editor.ps1, Install_Editor.cmd,
Enable_Editor.cmd and Disable_Editor.cmd
  The exact released Windows installer and loader-toggle helper source.
Source/Packaging/make_payload_manifest.py
  The released payload allow-list generator.
ThirdParty/
  The release's expanded corresponding source, licenses, attribution and
  provenance for its loader and interoperability components. Other bundled
  dependency notices are retained here as in the original release.
Network_Disclosure.txt
  The loader's reference-download rationale, URL and source review locations.
BUILDING_SOURCE_REVIEW.txt
  Concrete build prerequisites and commands for this reduced review package.
RELEASE_README.txt and VALIDATION.txt
  Original release instructions, the player's test report and known limits.
Verification/
  Original build and validation records; these are historical release results,
  not a claim that the reduced review package has been installed or retested.
PayloadManifest.json and PUBLIC_RELEASE_SHA256SUMS.txt
  Exact original release manifests. They intentionally list runtime files
  that are absent from this review package.
SOURCE_ORIGIN_MANIFEST.json
  Maps each retained file to its original public ZIP entry, size and SHA-256.
SOURCE_REVIEW_VALIDATION.json and SOURCE_REVIEW_SHA256SUMS.txt
  Checks for this review package and checksums of its distributed files.

The original files were copied byte for byte from the identified public ZIP.
This review README and BUILDING_SOURCE_REVIEW.txt are additional guidance.
Original Source/Editor/BUILDING.txt remains unchanged for traceability; its
Payload and packaging steps refer to the full release, not this reduced ZIP.

BINARY COMPILE STUBS INCLUDED WITH UPSTREAM SOURCE
------------------------------------------------
This archive is not literally binary-free. It retains two identical upstream
Il2Cppmscorlib.dll compile stubs at:
ThirdParty/Loader/Source/Il2CppInterop-1.5.3/Il2CppInterop.Runtime/Libs/
ThirdParty/InteropCompatibility/Source/Il2CppInterop-PR291/Il2CppInterop.Runtime/Libs/

Each file is 2,960,896 bytes with SHA-256:
EE6176648F56660E32DC354A9063197EE2C2022F8EC8DF3B177516D0FE671948

These are generic files distributed in the upstream Il2CppInterop source,
retained to preserve its corresponding build inputs. They are not President
Simulator code and cannot replace the generated game references needed to
compile the editor. Upstream project logos also remain in their source trees.
No game executable, GameAssembly.dll, game metadata, generated game-specific
wrappers, saved games or gameplay screenshots are included.

NETWORK REVIEW
--------------
The original editor and installer contain no mod auto-updater. The loader
downloads matching Unity reference libraries when its local cache needs them.
For this supported game, the default URL is:
https://unity.bepinex.dev/libraries/6000.3.9.zip

Inspect Network_Disclosure.txt and the included BepInEx source file:
ThirdParty/Loader/Source/BepInEx/Runtimes/Unity/
BepInEx.Unity.IL2CPP/Il2CppInteropManager.cs
The relevant members are UnityBaseLibrariesSource and DownloadUnityAssemblies.

BROWSER UPLOAD ITEMS
-------------------
To make this material available for reviewer inspection in a public GitHub
repository through its browser upload interface, upload these two files:
1. PresidentValuesEditor_v0.1.1_SourceReview.zip, unchanged.
2. README_NEXUS_REVIEW.txt, extracted from the root of that ZIP.

The README can be read on the repository page; reviewers can download and
extract the ZIP to inspect the source and BUILDING_SOURCE_REVIEW.txt. No
publication or staff communication is performed by these files themselves.

ATTRIBUTION
-----------
The original editor code/UI and listing were drafted with ChatGPT; the player
performed the reported in-game tests. Upstream dependencies remain the work
of their respective authors. Source/LICENSE.txt covers original editor/helper
material; the retained ThirdParty notices and licenses cover those components.
