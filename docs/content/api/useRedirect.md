---
title: "useRedirect"
weight: 2
date: 2019-09-27T15:06:34-07:00
---

This hook causes a browser redirect to occur if its `predicateUrl` matches.

## API

```typescript
export function useRedirect(
  predicateUrl: string,
  targetUrl: string,
  queryParams?: QueryParam | URLSearchParams,
  replace?: boolean
): void
```

## Basic

If `predicateUrl` is the current path, redirect to the `targetUrl`. `queryObj` is optional, and uses the same serializer that `useQueryParams` uses by default. If `replace` (default: true) it will replace the current URL (back button will skip the `predicateUrl`).

```jsx
import { useRedirect } from 'raviger'

function Route () {
  // Will redirect to '/new' if current path is '/old'
  useRedirect('/old', '/new', { name: 'kyeotic' })
  return <span>Home</span>
}
```

