---
layout: default
title: Technische Details
---

# Technische Dokumentation

## Architektur & Stack 🏗️

### Frontend
- **Framework**: Next.js/React
- **Styling**: Tailwind CSS + shadcn/ui
- **Features**:
  - Progressive Web App (PWA)
  - Clientseitige Bildkompression
  - Sichere Direkt-Uploads (Signed URLs)
  - MapLibre/Mapbox Integration
  - Responsive Design

### Backend
- **API**: 
  - REST/GraphQL Endpoints
  - OAuth2/JWT Authentication
  - Rate Limiting
  - Swagger/OpenAPI Docs

- **Datenbank**:
  - PostgreSQL mit pgvector Extension
  - Alternativ: OpenSearch für Vektor-Suche
  - Optimierte Indizes für Geo-Queries

- **Storage**:
  - S3-kompatibles Object Storage
  - Automatische Bildverarbeitung
  - CDN-Integration

### KI-Pipeline
1. **Vorverarbeitung**:
   - Bildqualitätsprüfung
   - NSFW/Spam-Erkennung
   - EXIF-Bereinigung

2. **Feature Extraction**:
   - Tierart-Klassifikation
   - Merkmalsvektoren-Generierung
   - Metadaten-Extraktion

3. **Matching-Engine**:
   - Vektor-Ähnlichkeitssuche
   - Geo-basiertes Filtering
   - Score-Berechnung

4. **Verarbeitung**:
   - Worker/Queue System (Celery/Sidekiq)
   - GPU-Inference (Managed Service)
   - Auto-Scaling

## Kommunikation & Benachrichtigungen 📡

### Messaging
- **E-Mail**: Transactional Mail Service
- **Push**: WebPush/APNs/FCM
- **SMS/Voice**: Telephony Provider
- **Privacy-Relay**: Masked Calling System

### Echtzeit-Updates
- WebSocket-Verbindungen
- Server-Sent Events
- Push-Notifications

## Betrieb & Qualitätssicherung 🛠️

### Deployment
- **CI/CD Pipeline**:
  - Automatisierte Tests
  - Code Quality Checks
  - Security Scanning

- **Umgebungen**:
  - Development
  - Staging
  - Production

- **Deployment-Strategie**:
  - Blue/Green Deployments
  - Automatische Rollbacks
  - Feature Flags

### Monitoring
- **Metriken**:
  - API Latenzen (P95)
  - Error Rates
  - User Engagement

- **Logging**:
  - Strukturierte Logs
  - Distributed Tracing
  - Error Tracking

- **Alerts**:
  - Performance Anomalien
  - Error Spikes
  - Kapazitätswarnung

### Testing
- Unit Tests
- API Contract Tests
- Visual Regression Tests
- E2E Tests (Cypress/Playwright)
- Load Tests

## Performance-Ziele 📊

- **Latenz**:
  - API: P95 < 500ms
  - KI-Inference: < 3s
  - First Contentful Paint: < 1.5s

- **Verfügbarkeit**:
  - System: 99.9%
  - API: 99.95%
  - Datenbank: 99.99%

- **Skalierung**:
  - 100k concurrent users
  - 1M Bilder/Tag
  - 50k Matches/Tag

[Datenschutz & Sicherheit ansehen](/privacy)