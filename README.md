---
description: Provides complete list.
---

# Suspense and Concurrent mode

## Relay

* Allows to develop data driven application for react.

## Relay and data fetching with Suspense

* Library authors can use for data fetching libraries.

## What problems solved?

* Creates a **good loading experience**
* A balance between showing essential short data when obtained and the janky loading experience.
* Initially what react does is called **Fetch on render** 1. React renders the component while calling life cycle methods and those methods calls API. 2. and once api obtained rendering is made 3. then its children component starts to do from **step 1** and keeps on loading. 4. It causes **Waterfall**
* What relay does is \(_using GraphQL in Fragment hook_\)
  * fetching essential data before.
  * Then once all data is obtained then the entire UI is shown, rather than showing one by one and others get loading.
  * Here what we does is **Fetch then render**
* Both these cases are at its extreme. That's why here comes **Suspense.**
* You can also order suspense using **Suspense ordering.**.

```javascript
Component/Container {
  return (
    <ErrorBoundary fallback={(<ErrorMessage />)}>
      <SuspenseList revealOrder="forwards"> // backwards for reverse of it.
        <Suspense fallback={<ComposerFallback />}>
          <Composer />
        </Suspense>
        <Suspense fallback={<FeedFallback />}>
          <Feed />
        </Suspense>
      </SuspenseList>
    </ErrorBoundary>
  )
}
```

### Suspense for new page.

* If we follow above pattern here then it will be like
  * render -&gt; get list of fetches -&gt; calls fallback -&gt; _Once done_ -&gt; Changes actual datas in place holder.
* This is actually moving us back to the **Fetch on render** schema.
* What we need is to **render** and **fetch data** in parellel and render data ASAP.
* This way is called as **Render as you fetch** this is what **React SUspense** is for.

## Use suspense for Data fetching

### `useQuery`Suspense and Concurrent mode



