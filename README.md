# Provider import link evidence (#5428)

Synthetic provider data only. No real hub, account, token, or provider key was used.

Tested feature commit: `d4f370d1b` (including `origin/main` through `6b4db662a`). Any later merge-only synchronization with `main` leaves the feature diff unchanged.

## iOS

`ProviderImportLinkUITests` runs on an iPhone 17 / iOS 27.0 simulator against the local mock hub. Each capture follows the real external deep link and checks the prefilled provider and that the mock's provider list is unchanged before Save. The stock notification-permission prompt is dismissed first.

| Text size | Light | Dark |
| --- | --- | --- |
| Default | [image](ios/persona-import-wizard-light.png) | [image](ios/persona-import-wizard-dark.png) |
| Accessibility XXXL | [image](ios/persona-import-wizard-light-ax.png) | [image](ios/persona-import-wizard-dark-ax.png) |

## Android

`ProviderPasteShotsTest` drives the real Compose provider flow with a fake API. It checks that the secret-bearing link is not rendered, that a second link replaces the first review, and that no provider is added before Save.

| Flow | Light | Dark |
| --- | --- | --- |
| Link review, default text | [image](android/provider-import-link-review-light.png) | [image](android/provider-import-link-review-dark.png) |
| Link review, 2x text | [image](android/provider-import-link-review-light-ax.png) | [image](android/provider-import-link-review-dark-ax.png) |
| Prefilled provider, default text | [image](android/provider-import-link-prefill-light.png) | [image](android/provider-import-link-prefill-dark.png) |
| Prefilled provider, 2x text | [image](android/provider-import-link-prefill-light-ax.png) | [image](android/provider-import-link-prefill-dark-ax.png) |
