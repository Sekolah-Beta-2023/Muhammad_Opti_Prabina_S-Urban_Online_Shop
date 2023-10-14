
## App Setup (localhost)

```
SUPABASE_URL="https://podfjzvbjovtumjbznew.supabase.co"
SUPABASE_KEY="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InBvZGZqenZiam92dHVtamJ6bmV3Iiwicm9sZSI6ImFub24iLCJpYXQiOjE2OTcyMDA5NTMsImV4cCI6MjAxMjc3Njk1M30.xabMBOl1nsqsMRc-M-PdP30sCQQsYaXL9LMg0PQ-2xU"


DATABASE_URL="postgresql://postgres:fzTNFq5QOw8Vz18P@db.podfjzvbjovtumjbznew.supabase.co:5432/postgres"

git clone https://github.com/optisamosir/tugasakhir

cp .env.example .env

npm i

npx prisma generate

npm run dev
```

You'll have to setup a Supabase account & Stripe account, then add all of the details in to your .env file.

Once you've connected your application to Supabase. You'll also need to setup the Auth Providers:
    Google [Google](https://cloud.google.com)
    Github [Github](https://github.com/settings/developers)
    
    https://supabase.com/docs/guides/auth/social-login/auth-google
    https://supabase.com/docs/guides/auth/social-login/auth-github
    
Now run the command to migrate your database tables and run your seed file.
    
```
npx prisma migrate dev --name init
```