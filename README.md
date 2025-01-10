# React useEffect setInterval Bug

This repository demonstrates a common bug in React applications involving the use of `setInterval` within the `useEffect` hook.

## Bug Description
The `MyComponent` uses `setInterval` to update a counter every second. However, the component has an empty dependency array [] in `useEffect`, meaning the `setInterval` is only called once during the component's mount.  The closure over the `count` variable causes issues because the `count` value used in `setInterval` is not the latest value of count, resulting in the counter not updating correctly.