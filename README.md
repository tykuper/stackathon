# Stackathon

## Notes

### TypeScript

- In javascript, types don't need to be declared and the code is interpreted at runtime. A program and won't catch certain errors until it is run and the browser throws the error.

- Typescript extends javascript (TypeScript is a superset of javascript) with types, and behaves like a compile language that turns it into javascript at runtime/bundling. This is really helpful in preventing a lot of errors, and has an additional benefit of much better autocomplete usability in VS code.

- AngularJS (a popular framework) is not supported moving forward in favor of Angular - this framework is TypeScript only.

- Next.js can use either JS or TS, but is better suited for typescript, and also allows for additional features.

### Next.js - framework built on top of Node.js

- React without next.js - entire bundle gets delivered to user whenever they enter the website. Can take a while for heavier bundles (spinning/loading is frequently seen by the user - javascript on client side is pulling in data and then rendering which can be slow)
- In next.js, individual pages are pre-rendered- next.js does page splitting by default. The pages are pre-built/rendered on a server (like Vercel) per request. Much faster for the server to do this than your browser/client. Because the html is generated in advance, this also results in improved SEO.
  - Static generation
    - Html generated on build and reused for each request
    - Quicker to load, makes more sense if the information on the page is static (hence the name), since we don't need to have the information on the page rebuilt
    - Can be cached on a CDN - much quicker to have the cached pages on a server geographically closer to the requesting location
  - Server-Side Rendering
    - Html generated per request
    - Slower than static generation, but needs to be done if the information needs to be frequently updated.
  - Both static and server-side can be done in the same application
    - Use static as much as possible for best performance

## My project

- Blog site:

https://user-images.githubusercontent.com/94147433/184623281-2421b073-b31b-4c9c-859e-8a2c346eac41.png

- Sanity.io used as a headless CMS in lieu of express/postgres
  - Useful for non-technical users to add in information themselves and view the data

https://user-images.githubusercontent.com/94147433/184623290-c726ae23-a98c-4b98-a9c3-d9481a15df44.png

- Pull the data into the program using GROQ (similar to graphQL)

https://user-images.githubusercontent.com/94147433/184623302-b260a3ec-b17a-49c5-9e9b-c5cda359f2a6.png
