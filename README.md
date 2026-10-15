# Telegram Hosting Bot — Railway Repository

## Files
- `33rd.py` — bot source
- `requirements.txt` — Python dependency
- `Procfile` — Railway worker start command

## Deploy
1. Create a new GitHub repository.
2. Upload these three files to the repository root.
3. In Railway, create a project from that GitHub repository.
4. In the Railway service Variables, add:
   - `BOT_TOKEN` = a NEW token from @BotFather
   - `ADMIN_ID` = your numeric Telegram user ID
5. Deploy and inspect the deployment logs.

## Important
- The original source contained a hardcoded Telegram bot token. This packaged copy requires `BOT_TOKEN` from Railway Variables instead. If the old token was real or shared, revoke it through @BotFather and use a new one.
- The SQLite database and uploaded scripts need persistent storage for reliable retention across redeploys. This project has not been modified to move its database/files onto a Railway Volume yet.
- This bot executes Python files uploaded by Telegram users and attempts to install packages for those files. Only run it with trusted uploads and review Railway resource/security limits.
- Hosting costs and always-on behavior depend on the current Railway plan and usage limits.
