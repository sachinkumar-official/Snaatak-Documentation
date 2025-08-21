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

## Table of Contents
- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Implementation Guide](#implementation-guide)
  - [Base Installation](#1-base-installation)
  - [Configuration Files](#2-configuration-files)
  - [Update package.json Scripts](#3--update-packagejson-scripts)
  - [Sample Test File](#4--sample-test-file)
  - [Running Tests](#5--running-tests)
- [Contact Information](#contact-information)
- [References](#references)

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
<img width="887" height="402" alt="Image" src="https://github.com/user-attachments/assets/50d02ac8-5c45-4c4e-93a1-82d12c121d04" />

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
<img width="688" height="204" alt="Image" src="https://github.com/user-attachments/assets/fbbe755f-a367-47e9-8ac0-54b0de07d7ec" />

#### `jest.setup.js`

```bash
require('@testing-library/jest-dom/extend-expect');
```
<img width="456" height="43" alt="Image" src="https://github.com/user-attachments/assets/f8495744-3eea-4a7a-b20e-8806ada8c2f4" />

### 3.  Update package.json Scripts

```bash
"scripts": {
  "test": "jest",
  "test:watch": "jest --watch",
  "test:coverage": "jest --coverage"
}
```
<img width="705" height="525" alt="Image" src="https://github.com/user-attachments/assets/f75a1fbe-36c0-43d1-8db0-0b31c78353cf" />

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
<img width="705" height="525" alt="Image" src="https://github.com/user-attachments/assets/e68428fd-2dfc-4f63-a211-60a635289715" />

### 5.  Running Tests

```bash
npm test
```
<img width="404" height="279" alt="Image" src="https://github.com/user-attachments/assets/1c4f8f1e-10c1-466a-b8bc-4bdb62765722" />

---
## Contact Information
| Name            | Email Address                         |
|-----------------|---------------------------------------|
| Sachin Kumar  | [sachin.kumar.snaatak@mygurukulam.co](mailto:sachin.kumar.snaatak@mygurukulam.co) |

---

## References  

| Title                          | Link                                                                 |  
|--------------------------------|----------------------------------------------------------------------|  
| **Jest Documentation**       | [Visit](https://jestjs.io/) |  
| **React Testing Best Practices**                  | [Visit](https://legacy.reactjs.org/docs/testing.html) |  
