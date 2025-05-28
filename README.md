# a3-cloudsec-s3575564
# CloudSec Assignments

This repository contains two standalone, browser-based demos used for INTE2402 Assignment 3 (Cloud Security 2025):  

1. **Paillier Homomorphic Encryption** (Q1)  
2. **3-of-4 Shamir Secret Sharing** (Q2)  

Each demo is a self‑contained HTML/JavaScript application that runs entirely in your browser.

---

## 🗂️ Repository Structure

```
CloudSec/
├── index.html                       ← Landing page with links to both demos
├── a3-q1-paillier-encryption.html   ← Paillier demo (Q1)
├── a3-q2-shamir-secret-share.html   ← Shamir demo (Q2)
├── .gitignore
└── README.md                        ← This file
```

---

## 🔧 Prerequisites

> No build step or external API keys are required—everything runs locally in your browser.

---

## ▶️ How to Run

To serve these static pages:

### 1) Using `npx serve`

1. Open a terminal in the **project root** (where this `README.md` lives).
2. Install the static server (if you haven’t already):

   ```bash
   npm install -g serve
   ```
3. Run:

   ```bash
   cd a3-cloudsec-s3575564
   npx serve .
   ```
3. In your browser, go to:

   ```
   http://localhost:3000
   ```
4. Click the demo link you want to explore.

---

## 📄 Demo Descriptions

# Q1 Paillier Homomorphic Encryption Tool

A simple browser-based demo of Paillier key generation & encryption

## Features

- Generate a Paillier key pair: p, q, N, φ(N), g, μ  
- Hash an input message (MD5 → truncated hex → BigInt)  
- Encrypt plaintext homomorphically: c = gᵐ · rᴺ mod N²  

## Prerequisites

- A modern web browser (Chrome, Firefox, Edge, Safari) with JavaScript enabled  
- No server or build step required

## Q2 Shamir Secret Sharing Demo

**File:** `a3-q2-shamir-secret-share.html`

An interactive 3-of-4 Shamir splitting and recovery tool that:

- Defines a secret `s` and polynomial coefficients `a`, `b` over a prime `p`  
- Computes four shares for `x = 1,2,3,4` using  
  \[
    y = a x^2 + b x + s \bmod p
  \]
- Allows you to pick any three shares and recover `s` via Lagrange interpolation  

### Usage

1. Open `a3-q2-shamir-secret-share.html` in your browser.  
2. Enter your secret `s`, coefficients `a`, `b`, and prime modulus `p`.  
3. Click **Get Polynomial Equation** to see the formula.  
4. Click **Compute 4 Points** to generate shares `(xᵢ, yᵢ)`.  
5. Fill in any three `(x, y)` pairs and click **Recover secret s**.  
6. Verify that the recovered value equals your original secret.

---

##  Support

If you run into any issues or have questions, please open an Issue in this repo. Happy exploring!
