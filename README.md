# Little Lemon Booking App

A responsive restaurant booking application built as the final capstone project for the **Meta Front-End Developer Professional Certificate**.

Little Lemon is a fictional family-owned Mediterranean restaurant that combines traditional recipes with a modern dining experience. This project adds an online booking feature for customers.

---

## Table of Contents

* [About](#about)
* [Getting Started](#getting-started)
* [Architecture](#architecture)
* [Folder Structure](#folder-structure)
* [Component Design](#component-design)
* [Naming Conventions](#naming-conventions)
* [Dependencies](#dependencies)
* [Data Management](#data-management)
* [Testing](#testing)
* [Future Improvements](#future-improvements)
* [Honor Code](#honor-code)

---

## About

This project was built as the final capstone for the Meta Front-End Developer Professional Certificate.

### Project Goal

Create a modern, responsive web application for **Little Lemon** with an online table booking experience.

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/AstridYami/Booking-a-Table-on-the-Little-Lemon-Website-Capstone.git

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm start
```

Run tests:

```bash
npm test
```

Run tests with coverage:

```bash
npm run test:cv
```

---

## Architecture

The project focuses on a simple, scalable frontend architecture.

Main design considerations include:

* Organized folder structure
* Reusable components
* Consistent naming conventions
* Minimal dependencies
* Centralized data management
* Unit testing

---

## Folder Structure

```
src/
├── actions/
├── assets/
├── components/
├── context/
├── hooks/
├── pages/
├── settings/
└── utilities/
```

### Components

Reusable UI components.

Each component typically contains:

```
Component/
├── Component.jsx
├── Component.css
├── Component.test.jsx
└── index.js
```

### Pages

Application screens built from reusable components.

Examples:

* Home
* Booking
* Confirmed Booking

### Context

Contains Context Providers and custom hooks for shared state.

### Hooks

Reusable custom hooks that are independent of Context.

### Actions

Reducer functions and initial application state.

### Utilities

Shared helper functions such as validation.

### Settings

Global configuration and mock CMS data used throughout the application.

---

## Component Design

The application follows a reusable component-based architecture.

Key principles include:

* Small, focused components
* Separation of responsibilities
* Reusable nested components for complex UI
* Context API for form state management

Some components (such as `Table`) also support the Composite Component pattern for greater flexibility.

Example:

```jsx
<Table>
  <Table.Body>
    <Table.Header>
      <Table.Cell>ID</Table.Cell>
      <Table.Cell>Name</Table.Cell>
      <Table.Cell>Price</Table.Cell>
    </Table.Header>
  </Table.Body>
</Table>
```

The booking form uses a dedicated `FormContextProvider`, allowing form state to be shared across multiple form steps while remaining isolated from the rest of the application.

---

## Naming Conventions

### CSS Classes

Each component uses a root class following the format:

```
LL-Component
```

Nested elements extend this pattern:

```
LL-ComponentHeader
LL-ComponentBody
```

### Utility Classes

Reusable utility classes provide common styling such as typography:

```
text-sm
text-md
text-lg
text-xl
```

### CSS Variables

Global CSS variables are used for consistent spacing, colors, shadows, and other design tokens throughout the application.

---

## Dependencies

This project intentionally keeps external dependencies to a minimum.

* Custom CSS (no CSS framework)
* Custom form validation
* Utility helper functions
* Font Awesome for icons

No form libraries such as Formik or Yup were used.

---

## Data Management

Shared content is stored inside the `settings/cms` folder.

This simulates fetching content from a Content Management System (CMS), making it easier to replace with a real backend in the future.

---

## Testing

Testing is implemented using:

* React Testing Library
* Jest
* Jest DOM

Tests are located alongside their related components and pages.

Coverage includes:

* Components
* Context
* Reducers
* React hooks
* Form interactions

---

## Future Improvements

The application is designed to be easily extended.

Potential enhancements include:

* Multi-step booking flow
* Phone number verification
* OTP confirmation
* Backend API integration
* Database persistence
* Theme switching (Light/Dark Mode)
* Content management integration

The existing Context API and `useReducer` architecture make these additions straightforward.

Please use this repository for learning and reference purposes only. If you're currently completing the certification, avoid copying the solution directly to ensure you gain the intended learning experience.
