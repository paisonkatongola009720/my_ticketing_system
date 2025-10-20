# Professional Helpdesk Ticketing System

## Overview
A complete customer support platform built with Flask, featuring authentication, ticket management, knowledge base, and analytics. This is a comprehensive helpdesk solution for managing customer support requests with role-based access control.

## Current State
- **Status**: Fully functional Flask web application
- **Framework**: Flask with SQLAlchemy ORM
- **Database**: SQLite (development), ready for PostgreSQL in production
- **Port**: 5000 (configured for Replit environment)

## Recent Changes
- **2025-10-15**: UI/UX and Profile Management Updates
  - Converted navigation menu to dropdown in top-right corner
  - Added user profile page with ticket statistics
  - Added profile edit functionality with password change
  - Implemented backend validation for profile updates
  - Added missing VIEW_ARTICLE_TEMPLATE for knowledge base articles
  - Configured for 0.0.0.0:5000 (Replit-compatible)
  - Database and uploads directories included

## Project Architecture

### Core Components
1. **Authentication System**
   - User registration and login
   - Role-based access control (Admin, Agent, User)
   - Password hashing with Werkzeug

2. **Ticketing System**
   - Create, view, update tickets
   - Auto-assignment to agents
   - Priority-based SLA management
   - File attachments support
   - Comment system with internal notes
   - Ticket history tracking

3. **Knowledge Base**
   - Self-service articles
   - Category-based organization
   - Search functionality
   - View tracking

4. **Admin Features**
   - User management
   - Agent performance analytics
   - Ticket export to CSV
   - System-wide statistics

### Database Models
- **User**: Authentication and user management
- **Ticket**: Support ticket tracking
- **Comment**: Ticket discussions
- **Attachment**: File uploads
- **TicketHistory**: Audit trail
- **KnowledgeBase**: Help articles

### File Structure
```
/
├── ticketing_system.py    # Main application file
├── instance/
│   └── ticketing_system.db # SQLite database
├── uploads/               # File attachments
└── ticketing_system.log  # Application logs
```

## Default Users (Development)
- **Admin**: username: `admin`, password: `admin123`
- **Agent**: username: `agent1`, password: `agent123`
- **User**: username: `user1`, password: `user123`

## Features
- ✅ User authentication and authorization
- ✅ Role-based access control (Admin, Agent, User)
- ✅ Modern dropdown navigation menu
- ✅ User profile management with edit capabilities
- ✅ Password change with security validation
- ✅ Ticket creation and management
- ✅ Auto-assignment of tickets to agents
- ✅ Priority-based SLA deadlines
- ✅ File attachments
- ✅ Comments and internal notes
- ✅ Knowledge base with search
- ✅ Agent performance analytics
- ✅ Ticket export (CSV)
- ✅ Audit trail/history
- ✅ **Admin User Management**:
  - Delete users and agents with ticket reassignment
  - Activate/deactivate user accounts
  - Change user roles dynamically
  - Prevent admins from deleting themselves
- ✅ **SLA Monitoring Dashboard**:
  - Track overdue tickets in real-time
  - Monitor tickets approaching SLA deadlines (24h warning)
  - Role-specific views for admins and agents
- ✅ **Advanced Reports & Analytics**:
  - Ticket statistics by category and priority
  - Agent performance metrics with resolution rates
  - Average resolution time tracking
  - Comprehensive dashboard with visual stats

## Technical Stack
- **Backend**: Flask 3.x
- **Database**: SQLAlchemy ORM with SQLite
- **Security**: Werkzeug password hashing
- **Frontend**: Jinja2 templates (inline)
- **File Handling**: Secure file uploads with 16MB limit

## Environment Configuration
- Host: 0.0.0.0 (allows proxy access)
- Port: 5000 (Replit standard)
- Debug mode: Enabled for development
- Database: SQLite for development (easily switchable to PostgreSQL)

## User Preferences
- Clean, maintainable code structure
- Security best practices (no exposed secrets)
- Production-ready deployment configuration
