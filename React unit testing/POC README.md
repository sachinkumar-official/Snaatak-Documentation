# POC of React Unit Testing 

<img width="275" height="183" alt="Image" src="https://github.com/user-attachments/assets/01e0be40-e8e3-4667-af06-d49d6411797d" />

---
## Author Information
| Last Updated On | Version | Author       | Level           | Reviewer   |
|-----------------|---------|--------------|-----------------|------------|
| 20-08-2025      | V1.0    | Sachin Kumar | Internal Review | Pritam     |
| 21-08-2025      | V1.1    | Sachin Kumar | L0              |Shreya/Sharvari|
|                 |         | Sachin Kumar | L1              | Abhishek V |
|                 |         | Sachin Kumar | L2              | Abhishek Dubey/Rishabh sharma|
---

## Introduction
This POC demonstrates the implementation of Jest for unit testing React components, covering setup, configuration, and test execution.

## Pre-requisites
| Requirement         | Version/Details            |
|---------------------|---------------------------|
| **Node.js**             | ≥ v16.x                   |
| **npm or yarn**         | ≥ v8.x (npm) or yarn      |
| **React application**   | v17+ recommended          |

## Implementation Guide

### 1. Base Installation
```bash
npm install --save-dev \
  jest@26.x \
  @types/jest@26.x \
  @testing-library/react@12.x \
  @testing-library/jest-dom@5.x \
  @testing-library/user-event@13.x \
  jest-environment-jsdom@26.x \
  --legacy-peer-deps
```
![1](https://github.com/Nishkarsh9/images/blob/main/Screenshot%202025-05-21%20123037.png)
### 2. Configuration Files

#### `jest.config.js`

```javascript
module.exports = {
  testEnvironment: 'jsdom',
  setupFilesAfterEnv: ['<rootDir>/jest.setup.js'],
  moduleNameMapper: {
    '\\.(css|less|scss)$': 'identity-obj-proxy'
  },
  testPathIgnorePatterns: [
    '/node_modules/',
    '/public/'
  ]
};
```
![2]()
#### `jest.config.js`

```bash
require('@testing-library/jest-dom/extend-expect');
```
### 3.  Update package.json Scripts

```bash
"scripts": {
  "test": "jest",
  "test:watch": "jest --watch",
  "test:coverage": "jest --coverage"
}
```
![3](https://github.com/Nishkarsh9/images/blob/main/Screenshot%202025-05-21%20123343.png)
### 4.  Sample Test File
Create a test file for a React component in /frontend/src/components/__tests__/Example.test.js.
```bash
import React from 'react';
import { render, screen } from '@testing-library/react';
import Button from './Button';

test('renders button with text', () => {
  render(<Button>Click Me</Button>);
  expect(screen.getByText('Click Me')).toBeInTheDocument();
});
```
![4](https://github.com/Nishkarsh9/images/blob/main/Screenshot%202025-05-21%20123904.png)
### 5.  Running Tests

```bash
npm test
```
![5](https://github.com/Nishkarsh9/images/blob/main/Screenshot%202025-05-21%20130015.png)

---
## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](sachin.kumar.snaatak@mygurukulam.co) |

---

## References  

| Title                          | Link                                                                 |  
|--------------------------------|----------------------------------------------------------------------|  
| **Jest Documentation**       | [Visit](https://jestjs.io/) |  
| **React Testing Best Practices**                  | [Visit](https://legacy.reactjs.org/docs/testing.html) |  
