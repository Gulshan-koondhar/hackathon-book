# Physical AI & Humanoid Robotics Textbook - Deployment Guide

This repository contains the complete AI-native interactive textbook for Physical AI & Humanoid Robotics. This document provides information about the deployment setup.

## Repository Structure

- `physical-ai-robotics-book/` - Main Docusaurus project containing the textbook content
- `.vercel/` - Vercel deployment configuration
- `specs/` - Specification and planning documents

## Deployment

The site is deployed to Vercel with the following configuration:

- **URL**: https://physical-ai-robotics-textbook-new.vercel.app
- **Build command**: `npm run build` (defined in package.json)
- **Output directory**: `build` (as specified in vercel.json)

## How to Deploy

1. The site is automatically deployed when changes are pushed to the `main` branch
2. For manual deployment, you can use the Vercel CLI:
   ```bash
   cd physical-ai-robotics-book
   vercel --prod
   ```

## Configuration Files

- `physical-ai-robotics-book/vercel.json` - Vercel deployment configuration
- `physical-ai-robotics-book/docusaurus.config.ts` - Docusaurus site configuration
- `physical-ai-robotics-book/package.json` - Build scripts and dependencies

## Technologies Used

- Docusaurus v3.9.2
- React v19
- Node.js >=20.0
- Vercel for deployment