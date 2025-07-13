# Igor Sharin
![Photo](./assets/photo.jpg)

## Contacts
* **Phone**: +7(996)-316-38-50
* **Email**: sharinigor1@gmail.com
* **GitHub**: [https://github.com/ImbaSharikAnirum](https://github.com/ImbaSharikAnirum)
* **Linkedin**: [www.linkedin.com/in/igor-sharin](https://www.linkedin.com/feed/?trk=guest_homepage-basic_nav-header-signin)
* **Telegram**: @igor_sharin

## About Me
I started programming on my own and now I want to build a strong foundation of knowledge to confidently write clean and understandable code. For me, it's important not just to know the syntax but to apply best practices and architectural solutions. I also plan to improve my understanding of algorithms and data structures to create efficient solutions.

## Skills
* React, Redux, Material UI (MUI), Bootstrap, HTML, CSS, i18n
* Node.js, Strapi, Django, Python
* Socket.IO, Webhooks, REST API
* AWS S3, Heroku, Railway
* Git, GitHub  

## Projects
* [RS School CV#1. Markdown & Git](https://imbasharikanirum.github.io/rsschool-cv/cv)

## Code Example

```
export const creationAPI = createApi({
  reducerPath: "creation",
  baseQuery: fetchBaseQuery({
    baseUrl: API,
    prepareHeaders: (headers, { getState }) => {
      const token = selectJwt(getState());
      if (token) {
        headers.set("authorization", `Bearer ${token}`);
      }
      return headers;
    },
  }),
  tagTypes: ["creation"],
  endpoints: (builder) => ({
    getCreations: builder.query({
      query: ({ userId, page = 1 } = {}) => {
        let url = `/creations?pagination[page]=${page}&pagination[pageSize]=30&populate[image]=*&sort=publishedAt:desc`;
        if (userId) {
          url += `&filters[users_permissions_user][id][$eq]=${userId}`;
        }
        return { url, method: "GET" };
      },
      providesTags: ["creation"],
    }),
  }),
});
```

## Education

**2016 - 2018**
Master's degree / Tourism
North-Eastern Federal University, Faculty of Law

**2012 - 2016**
Bachelor's degree / Jurisprudence
North-Eastern Federal University, Faculty of Law

## English
Pre-Intermediate
