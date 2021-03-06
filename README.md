# Hatina

The service for sharing fakenotes from [fakenote-studio].

[fakenote-studio]: https://github.com/stampylongr/fakenote-studio

## Configuration

Set up Firebase:

- Create a project at the [Firebase console](https://console.firebase.google.com/).
- Copy the contents of `.env.local.example` into a new file called `.env.local`
- Get your account credentials from the Firebase console at _Project settings > Service accounts_, where you can click on _Generate new private key_ and download the credentials as a json file. It will contain keys such as `project_id`, `client_email` and `private_key`. Set them as environment variables in the `.env.local` file at the root of this project.
- Get your authentication credentials from the Firebase console under _Project settings > General> Your apps_ Add a new web app if you don't already have one. Under _Firebase SDK snippet_ choose _Config_ to get the configuration as JSON. It will include keys like `apiKey` and `authDomain`. Set the appropriate environment variables in the `.env.local` file at the root of this project.
- Go to **Develop**, click on **Realtime Database** and create a database if you don't already have one. Under _data_ get `databaseUrl`(e.g. `https://[dbname].firebaseio.com/`). Set the appropriate environment variables in the `.env.local` file at the root of this project.
- Go to **Develop**, click on **Authentication** and in the **Sign-in method** tab enable authentication for the app.

Install it and run:

```bash
$ npm install
$ npm run dev
# or
$ yarn
$ yarn dev
```

Deploy it to the cloud with [Vercel](https://vercel.com/new?utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).

After deploying, copy the deployment URL and navigate to your Firebase project's Authentication tab. Scroll down in the page to "Authorized domains" and add that URL to the list.
