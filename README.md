# brod-releases

Публичные подписанные данные для клиента Brod: сейчас — список источников подписок (`sources.json`), позже — манифест релизов.

Клиент забирает `sources.json` и `sources.json.sig` раз в сутки и **принимает список только с верной подписью ed25519** ключа автора, вшитого в программу. Подмена файла в этом репозитории или по дороге без закрытого ключа ничего не даёт. Номер `version` растёт с каждой публикацией; клиент не применяет список старее уже применённого.

Здесь нет ни узлов, ни паролей, ни персональных адресов: только публичные адреса списков (GitHub raw, зеркала, публичные каналы Telegram).

Проверить вручную (нужен открытый ключ автора):

```
base64 -d sources.json.sig > sig.bin   # подпись ed25519 над точными байтами sources.json
```

Открытый ключ: `sXyEgNh66O+orP+JCOMk+rEdrfsyPqFKNWm98asb4aM=`

---

Public signed data for the Brod client: a list of subscription sources (`sources.json`), later a release manifest. The client accepts a document only if its ed25519 signature (`*.sig`) verifies against the author's public key embedded in the app, and only if `version` is newer than the one already applied. No secrets or personal data here — only public list URLs.
