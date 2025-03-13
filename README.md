{
  "manifest_version": 2,
  "name": "GitHub Replace Button",
  "version": "1.0",
  "description": "在 GitHub 文件页面添加 Replace 按钮，刷新页面才会出现",
  "permissions": [
    "activeTab",
    "storage",
    "https://api.github.com/*"
  ],
  "content_scripts": [
    {
      "matches": ["*://github.com/*/blob/*"],
      "js": ["content.js"],
      "css": ["styles.css"],
      "run_at": "document_end"
    }
  ],
  "options_ui": {
    "page": "options.html",
    "browser_style": true
  },
  "icons": {
    "32": "icon/icon32.png",
    "48": "icon/icon48.png",
    "128": "icon/icon128.png"
  },
  "browser_action": {
    "default_icon": {
      "32": "icon/icon32.png",
      "48": "icon/icon48.png",
      "128": "icon/icon128.png"
    },
    "default_title": "GitHub Replace Button"
  },
  "browser_specific_settings": {
    "gecko": {
      "id": "github-replace-button@example.com"
    }
  }
}
