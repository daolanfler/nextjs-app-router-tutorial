## Server Actions

React Server Actions allow you to run asynchronous code directly on the server. The eliminate the
need to create API endpoints to mutate your data. Instead, you write asynchronous functions that
execute on the server and can be invoked from your Client or Server Components.

Next.js with Server Actions

Sever Actions are also deeply integrated with Next.js caching. When a form is submitted through a
Server Action, no only can you use the action to mutate data, but you can also revalidate the
associated cache using APIs like `revalidatePath` and `revalidateTag`

Next.js has Client-side Router Cache that stores the route segments in the user's browser for a time
Since you're updating the data displayed in the invoices route, you want to clear this cache and
trigger a new request to the server. You can do this with the `revalidatePath` function from Next.js

## Error Handling

The `error.tsx` file can be used t odefine aUI boundary for a route segment. It serves as a catch-all
unexpected errors and allows you to display a fallback UI to your users.
