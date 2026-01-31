# 📘 Vue.js Learning Journal

---

## 📅 Phase 1: Project Setup & Basics

I started learning Vue.js by setting up a project using the official Vue CLI command:

```bash
npm create vue@latest

```

📦 Phase 2: Understanding Vue Components

I learned that every Vue component is composed of three main sections:

`1. <template>`

Contains the HTML-like structure of the UI

Vue compiles the template into real DOM elements

Dynamic values are rendered using {{ }}

`2. <script>`

Contains JavaScript logic such as:

Variables (state)

Imports

Functions

Component logic

`3. <style>`

Used for styling components

Can be scoped to avoid CSS conflicts across components


🧩 Phase 3: Composition API & <script setup>

I am currently working with the Composition API, which is the modern and recommended approach in Vue.

Although I haven’t studied the Options API in detail yet, I plan to learn and compare it later. For now, my focus is fully on the Composition API.

While using <script setup>, I learned that:

Components are automatically exported

There is no need to write export default

Components are imported using their file name

Variables defined in <script setup> are automatically available in the template

🔁 Phase 4: Reactive State

So far, I have created reactive variables using ref().

ref() is used to make primitive values reactive

.value is required when accessing or updating a ref in the script

.value is not required inside the template

I have not explored reactive() yet, but I plan to learn:

The difference between ref() and reactive()

When to use each one

♻️ Phase 5: Reusable Components

To make components reusable, I learned two core concepts:

1. Props

Props allow data to be passed from parent to child components

Defined using defineProps() inside <script setup>

Can specify:

Prop name

Type

Default value

Mainly used for passing:

Strings

Numbers

Booleans

Objects

2. Slots

Slots allow passing HTML or components into reusable components

Slots are more flexible than props

Props pass data, slots pass UI

Slots allow parents to control layout and structure


⚡ Phase 6: Actions & Events

I implemented a simple counter application, where I learned:

How to use @click to handle user actions

How to update reactive values using .value

How Vue automatically updates the UI when state changes


📝 Phase 7: Handling User Input

I learned two ways to handle user input:

1. Using @input

Handled input manually using:

@input

event.target.value

2. Using v-model

Provides two-way data binding

Keeps input and state in sync

Cleaner and more readable than manual input handling


✅ What I Have Learned So Far (Summary)

Vue project setup

Component structure (template, script, style)

Composition API and <script setup>

Reactive state with ref()

Component imports and usage

Props for reusability

Slots for flexible UI composition

Event handling with @click

Input handling with @input

Form handling with v-model




🎯 What I Should Learn Next (Roadmap)
🔜 Immediate Next Topics

reactive() vs ref()

computed() properties

v-if, v-show, v-for

Reusable input components

Basic form validation

🔜 Intermediate Topics

emit (child → parent communication)

v-model in custom components

Lifecycle hooks

Component communication patterns

🔜 Advanced Topics (Later)

State management basics

API integration

Vue Router

Performance optimization & best practices