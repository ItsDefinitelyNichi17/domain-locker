# Simple-Domain-Locker
## What it does?
An extension used to block certain domains, you can add your own list inside [rules.json](rules.json).
## Why it has no UI? you cannot configure it through the extension itself, hardcoded
* I want it to be simple and easy to use, without having multiple domains easily be unlocked through UI. The system is hidden behind the extension, so you cannot configure it through the extension itself.
## How to use?
* Enter your own list of domain to block 
```json
{
    "id": 1,
    "priority": 1,
    "action": { "type": "block" },
    "condition": {
      "urlFilter": "||example.com",
      "resourceTypes": ["main_frame"]
    }
}
```
* You can add it on your extension settings as a debug addons, installing it requires too many configurtaion. Whenever you restart or exit the browser, extension will be disabled.
## Resource
* [declerativeNetRequest](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest)
