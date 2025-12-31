# Yomi - Manga Reader for Android

## Overview

Yomi is a free, open-source manga reader application for Android devices. It provides access to 1200+ online manga sources, offline reading capabilities via downloads and CBZ archives, and integrates with tracking services like AniList, MyAnimeList, Shikimori, and Kitsu. The app features a Material You UI optimized for phones, tablets, and desktop, with support for Android 6.0+.

**Note:** This project has been discontinued due to legal challenges from Kakao Entertainment Corp and Google's sideloading policy changes.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Platform & Language
- **Platform:** Native Android application
- **Minimum SDK:** Android 6.0 (API level 23)
- **Language:** Kotlin (based on project structure and Android conventions)

### Core Architecture Patterns
- **Manga Parsers:** External parser system maintained in a separate repository (kotatsu-parsers) supporting 1200+ manga sources
- **Offline Storage:** Local download capability with CBZ archive support for offline reading
- **Data Synchronization:** Cross-device sync functionality tied to user accounts
- **Security:** Password and fingerprint-protected app access

### UI Framework
- **Design System:** Material You (Material Design 3)
- **Device Support:** Responsive layouts optimized for phones, tablets, and desktop form factors
- **Reader Modes:** Standard and Webtoon-optimized reading modes with gesture support

### Data Management
- **User Data:** Favorites organized by user-defined categories, reading history, bookmarks
- **Privacy:** Incognito mode support for private reading sessions
- **Notifications:** Chapter update notifications with updates feed

### Testing
- **Instrumented Tests:** Android instrumentation tests using JSON test fixtures for manga and category data validation

## External Dependencies

### Manga Tracking Services
- **Shikimori** - Anime/manga tracking platform
- **AniList** - Anime/manga database and tracking
- **MyAnimeList** - Anime/manga community and tracking
- **Kitsu** - Anime/manga discovery and tracking

### External Repositories
- **kotatsu-parsers** - Separate repository containing manga source parsers (1200+ sources)

### Translation Platform
- **Weblate** - Community-driven translation management at hosted.weblate.org

### Content Format Support
- **CBZ Archives** - Third-party comic book archive format for offline reading

### Development Considerations
- APK size optimization is prioritized - avoid adding unnecessary dependencies
- Performance takes precedence over code aesthetics
- New manga sources are added via the kotatsu-parsers repository, not the main app