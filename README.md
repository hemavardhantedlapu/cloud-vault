# Cloud-Vault - Smart Storage for 32GB Phones
**Member 1: Backend & Cloud Storage**

## Problem
32GB phone = 12GB OS + 8GB WhatsApp + 4GB Photos = 2GB free only. Game needs 7GB. How to play?

## My Solution: Streaming
Like Netflix streams movies, we stream games level-by-level and songs one-by-one from Supabase Cloud.

## What I Built

### 1. getGameLevel Function
Link: https://ctyqhqrzngfafxmrcetv.supabase.co/functions/v1/getGameLevel?level=1
- Returns only 200MB Level 1, not full 1GB game
- Saves 800MB storage
- Use ?level=2 for Level 2

### 2. streamsong Function
Link: https://ctyqhqrzngfafxmrcetv.supabase.co/functions/v1/streamsong?songId=1
- Streams 1 song (50MB)
- Before: 500MB for 100 songs
- Saves 90% storage

### 3. Personal Cloud Vault
- Bucket: cloud-vault-frontend-hosting (website)
- Bucket: cloud-vault-files-private (personal storage)
- Proof: Uploaded screenshot inside private bucket
- User can save his own movies/songs/photos and stream anytime

## Tech Stack
Supabase Edge Functions (Deno) + Storage

## Result
32GB phone can play 7GB games and store unlimited data!

#### How It Works - Workflow
Sir, we solve storage problem by streaming. We download 200MB level, play, delete, download next. Same for songs. Personal vault bucket lets user save his own movies/songs like Google Drive.
