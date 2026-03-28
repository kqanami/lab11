# Lab 11.1: Expo Setup and Core Components

**Student Name:** ____________________
**Student ID:** ____________________
**Date:** 28.03.2026

## Project Overview

This is a React Native mobile application built with Expo and TypeScript. The app demonstrates core React Native components by implementing a profile screen with a profile card and a contact form.

## Core Component Differences: React (Web) vs React Native

| Aspect           | React (Web)             | React Native                  |
|------------------|-------------------------|-------------------------------|
| **Renderer**     | DOM                     | Native iOS/Android components |
| **Container**    | `<div>`                 | `<View>`                      |
| **Text**         | `<p>`, `<span>`, `<h1>` | `<Text>`                      |
| **Images**       | `<img>`                 | `<Image>`                     |
| **Text Input**   | `<input>`, `<textarea>` | `<TextInput>`                 |
| **Scrolling**    | Native scroll / CSS     | `<ScrollView>`, `<FlatList>`  |
| **Buttons**      | `<button>`              | `<TouchableOpacity>`, `<Pressable>` |
| **Styling**      | CSS classes / files     | `StyleSheet.create()` API     |
| **Layout**       | CSS Flexbox (row default) | Flexbox (column default)    |
| **Click Events** | `onClick`               | `onPress`                     |
| **Lists**        | `.map()`                | `<FlatList>`, `<SectionList>` |

### Key Differences Explained

1. **No DOM Elements**: React Native does not use HTML. Instead of `<div>`, you use `<View>`; instead of `<p>`, you use `<Text>`. All text must be wrapped in `<Text>` components.

2. **StyleSheet API**: Instead of CSS files/classes, React Native uses `StyleSheet.create()` which validates styles at creation time and optimizes performance. Styles are JavaScript objects with camelCase properties.

3. **Flexbox Defaults**: In React Native, `flexDirection` defaults to `'column'` instead of `'row'` as in web CSS.

4. **No CSS Inheritance**: Unlike web CSS, styles don't cascade in React Native. Each component must be styled explicitly (except `Text` within `Text`).

5. **TouchableOpacity**: Web buttons have built-in click handling; React Native requires wrapping elements in `TouchableOpacity` or `Pressable` for touch interactions.

## Components

### ProfileCard (`src/components/ProfileCard.tsx`)
- Displays user avatar using `Image` component with remote URL
- Shows name and bio using `Text` components
- Renders stats (Posts, Followers, Following) in a horizontal `View` row
- Styled with `StyleSheet.create()` using shadow properties and Flexbox

### ContactSection (`src/components/ContactSection.tsx`)
- Three `TextInput` fields: email (email keyboard), phone (numeric keyboard), message (multiline)
- `TouchableOpacity` submit button with disabled state styling
- Success message displayed after submission
- Uses `useState` for form state management

## How to Run

```bash
cd ProfileApp
npm install
npx expo start
```

Scan the QR code with Expo Go app or press `a` for Android emulator / `i` for iOS simulator.

## Project Structure

```
ProfileApp/
├── App.tsx                          # Main app entry point
├── src/
│   └── components/
│       ├── ProfileCard.tsx          # Profile card with avatar and stats
│       └── ContactSection.tsx       # Contact form with text inputs
├── package.json
└── tsconfig.json
```
