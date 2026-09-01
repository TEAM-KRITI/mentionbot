# 🌈 Maya Mention — Full Bot

## Features
- Stylish start/help menu like the reference screenshots
- Add-to-group button
- Tag system: `/tagall`, `/tagadmins`, `/cancel`
- Couples: `/couple`, `/setcouple`, `/mycouple`, `/delcouple`
- Games: `/dice`, `/coin`, `/truth`, `/dare`, `/ship`, `/8ball`
- User tools: `/id`, `/info`, `/ping`
- Welcome system with `{name}`, `{mention}`, `{title}`
- Security guard: `/antispam`, `/lock links`, `/unlock links`
- SQLite database; no external database required
- Heroku worker configuration

## Heroku
1. Create a Heroku app.
2. Deploy this project.
3. Config Vars:
   - `BOT_TOKEN` = BotFather token
   - `BOT_USERNAME` = your bot username without @
   - `SUPPORT_URL` = your support group/channel URL
   - `UPDATE_URL` = your updates channel URL
4. Scale worker to 1:
```bash
heroku ps:scale worker=1 -a YOUR_APP_NAME
```

## Telegram permissions
For group features, add the bot to your group and make it admin.
For `/tagall`, the bot tags users it has observed in messages. Telegram's Bot API does not provide a general "list every member" endpoint, so a bot cannot magically fetch every group member.

## Important
This is an original implementation inspired by the visible menu/features. It does not copy private/proprietary source code from another bot.
