---
title: 'React — Hooks 使用技巧'
author: Zenan Lin
date: '06-15-2025'
image:
    url: '/images/image-2.webp'
    alt: 'React Hooks Tips'
---
## 概述

React Hooks 是 React 16.8 引入的特性，允许在函数组件中使用状态和其他 React 特性。

## useState

`useState` 是最基础的 Hook，用于在函数组件中添加状态：

```jsx
const [count, setCount] = useState(0);
```

## useEffect

`useEffect` 用于处理副作用，如数据获取、订阅或手动修改 DOM：

```jsx
useEffect(() => {
  document.title = `You clicked ${count} times`;
}, [count]);
```

## 自定义 Hook

自定义 Hook 是复用状态逻辑的最佳方式：

```jsx
function useWindowSize() {
  const [size, setSize] = useState({ width: 0, height: 0 });
  useEffect(() => {
    const handler = () => setSize({ width: window.innerWidth, height: window.innerHeight });
    window.addEventListener('resize', handler);
    return () => window.removeEventListener('resize', handler);
  }, []);
  return size;
}
```
