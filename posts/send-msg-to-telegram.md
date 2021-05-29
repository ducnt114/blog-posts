---
title: "How to send message to Telegram group"
date: 2021-02-15T16:46:47+07:00
categories: [coding, tutorial]
tags: [coding, tutorial]
---

## Create a Bot

Send message `/newbot` to BotFather

![create_bot](/telegram_1.png)

## Create a group chat and add Bot to group

![create_group](/telegram_2.png)

## Grant permission to Bot

![grant_permission](/telegram_3.png)

## Get chat group id

Using curl:

```bash
curl --location --request GET 'https://api.telegram.org/bot<BOT_TOKEN>/getUpdates'
```

response will be like:

```json
"chat": {
            "id": -1234567,
            "title": "MyTestZK Group",
            "type": "group",
            "all_members_are_administrators": true
    },
```

CHAT_ID will be `-1234567`

## Send message to group as bot

Using curl:

```bash
curl --location --request POST 'https://api.telegram.org/bot<BOT_TOKEN>/sendMessage?chat_id=<CHAT_ID>&text=<MESSAGE>'
```

or by code in Golang:

```go
func sendMessageToTelegram(msg string) error {
	botToken := os.Getenv("BOT_TOKEN")
	chatID := os.Getenv("CHAT_ID")
	postURL := fmt.Sprintf("https://api.telegram.org/bot%v/sendMessage?chat_id=%v&text=%v", botToken, chatID, msg)
	client := &http.Client{}
	req, _ := http.NewRequest("POST", postURL, nil)
	res, _ := client.Do(req)
	if res.StatusCode != http.StatusOK {
		return fmt.Errorf("Received bad status code: %v", res.StatusCode)
	}
	return nil
}
```
