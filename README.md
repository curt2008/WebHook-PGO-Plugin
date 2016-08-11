# WebHook-PGO-Plugin
A WebHook plugin that allows you to periodically send bot statistics to a third party webhook URL

## Using Plugins
Plugins are used by adding some new information to your `config.json`.

In your `config.json`, you can add a new array:

```
  ...
  "plugins": [
    "curt2008/WebHook-PGO-Plugin#2d54eddde33061be9b329efae0cfb9bd58842655"
  ],
  ...
```

Once that is there, you can add to your `tasks` array the task you want to use from the plugin. 
For instance, when using the WebHook PGO Plugin, you're going to use the following format:

```
  ...
  "tasks": [
    {
      "type": "WebHookPlugin.CustomWebhook",
      "config": {
      		"min_interval": 60,
      		"webhook_url": "http://www.website.com/webhook.php",
      		"stats": ["login", "uptime", "km_walked", "level_stats", "xp_earned", "xp_per_hour"]
      }
    }
  ]
  ..
```

Then just start the bot. It will download the specified plugin from this repository and use them when requested in your `tasks` list.
