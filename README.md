
# nextjs_app_prod
install pm2
pnpm add -g pm2

pm2 --version

cd ~/ai_annotator_tool
pm2 start "pnpm run start" --name annotator-ai
pm2 save
pm2 startup

Check if your app is running:
pm2 list

View app logs:
pm2 logs annotator-ai

Restart your app:
pm2 restart annotator-ai

Stop your app:
pm2 stop annotator-ai
