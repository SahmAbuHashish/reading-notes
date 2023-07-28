# Reading Questions

### Explain the concept of dynamic routes in Next.js and how they differ from static routes.

In Next.js, dynamic routes refer to pages that are created dynamically based on the values of certain parameters or segments in the URL. They allow you to create pages that share the same layout and design but display different content based on the provided parameters in the URL.

On the other hand, static routes are regular routes defined in Next.js without any dynamic placeholders.

Static routes represent fixed pages with predefined content that will be displayed regardless of the URL. These pages do not rely on dynamic segments and do not change their content based on URL parameters.

Differences between Dynamic Routes and Static Routes in Next.js:

---

### Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?

after Build the Next.js Application

1. Choose a Hosting Platform:
   - Vercel
   - Netlify
   - AWS Amplify

2. Configure the Deployment Platform: create an account on your chosen hosting platform, then connect your project repository.

3. Deploy the Application: Once your project is connected and configured, deploy the Next.js application to the hosting platform by running the deployment command or triggering the deployment through the platform's interface.

4. Verify and Test: After deployment, check that your Next.js application is live and working as expected. Test all the functionality to ensure that the deployment was successful.

---

### How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application.

- Next.js handles static file serving through a feature called "Static File Serving." By default, Next.js serves static assets like images, fonts, stylesheets, and other files directly from the `public` directory. The `public` directory is a special folder where you can place static assets that should be accessible to the client without going through the Next.js server.

- To reference static assets in a Next.js application, you can use relative URLs in your components or stylesheets. For example, to include an image located in the `public/images` directory, you can use the following:

```jsx
import React from 'react';

function MyComponent() {
  return (
    <div>
      <img src="/images/my-image.jpg" alt="My Image" />
    </div>
  );
}

export default MyComponent;
```