# Ready-to-Use Prompts

Copy and paste these prompts into Cursor to generate complete, production-ready applications.

## SaaS Dashboard

```
Build a SaaS analytics dashboard with:
- User authentication (sign up, login, logout)
- Organization/workspace management (create, invite team members)
- Analytics dashboard showing key metrics (visitors, revenue, growth)
- Settings page for billing and team management
- Dark mode support

Use PostgreSQL, Prisma, NextAuth.js, and shadcn/ui.
Include full test coverage for auth flows and API endpoints.
```

**What you get:**
- Multi-user auth with NextAuth
- Organization/multi-tenant architecture
- API endpoints with Zod validation
- React components with Tailwind styling
- Integration and E2E tests
- Database migrations

---

## AI Chat Application

```
Build an AI chat application where:
- Users can create multiple chat conversations
- Each conversation has a message history
- Messages are stored and retrieved with pagination
- Users can delete conversations
- Conversations are organized by date

Use Next.js 14, Prisma, PostgreSQL, and the Claude API.
Add dark mode and responsive design.
Include comprehensive test coverage.
```

**What you get:**
- Real-time messaging UI
- Conversation management API
- Streaming responses from Claude
- Message pagination
- Full database schema with proper indexes
- Component and API tests
- Dark mode support

---

## E-Commerce Product Catalog

```
Build an e-commerce catalog with:
- Product listing with search and filtering (category, price range, rating)
- Product detail page with reviews
- Shopping cart (client-side or persistent)
- Checkout flow
- Admin dashboard to manage products

Use PostgreSQL, Prisma, and shadcn/ui.
Include sorting, pagination, and real-time inventory.
```

**What you get:**
- Product and category models
- Search and filter API
- Review system with ratings
- Shopping cart management
- Admin CRUD endpoints
- Responsive product grid
- Full test coverage

---

## Project Management Tool

```
Build a project management app with:
- Users can create projects and invite team members
- Projects have tasks with status (todo, in-progress, done)
- Tasks can be assigned to team members
- Task comments and attachments
- Real-time notifications when tasks are updated

Use Next.js, PostgreSQL, Prisma, and WebSockets.
Include email notifications and mobile-responsive design.
```

**What you get:**
- Multi-tenant project architecture
- Task assignment and status tracking
- Comment system with notifications
- Real-time updates via WebSockets
- Email notification service
- Comprehensive CRUD APIs
- Dashboard UI with Kanban board
- Full test coverage

---

## Blog Platform with Comments

```
Build a blog platform where:
- Authors can write and publish posts
- Posts support markdown formatting with code syntax highlighting
- Readers can leave comments on posts (with moderation)
- Posts are organized by tags and categories
- Search functionality across posts and authors
- Author profiles with bio and social links

Use Next.js 14, Prisma, PostgreSQL, and shadcn/ui.
Include dark mode and a clean, modern design.
```

**What you get:**
- Post/Author/Comment/Tag models with proper relationships
- Markdown parser with syntax highlighting
- Search API with full-text search
- Comment moderation system
- Author profile pages
- Tag-based filtering
- SEO-friendly URLs
- Component and integration tests

---

## Internal Inventory System

```
Build an internal inventory management system with:
- Track products with SKU, quantity, location
- Barcode/QR code scanning
- Low stock alerts
- Purchase orders and receiving
- Inventory adjustments (damage, theft, etc.)
- Reports on stock movements

Use barcode scanning library and real-time notifications.
Include role-based access (Viewer, Manager, Admin).
```

**What you get:**
- Inventory schema with locations and stock tracking
- Barcode/QR scanning integration
- Purchase order workflow
- Stock adjustment audit trail
- Role-based API endpoints
- Real-time alerts for low stock
- Reports and analytics
- Mobile-responsive scanning interface

---

## Fitness Tracker

```
Build a fitness tracking app where:
- Users log workouts with exercises, sets, reps, weight
- Track progress over time with charts
- Create custom workout plans
- Social features: follow friends, compare progress
- Notifications for workout reminders
- Export workout history

Use Next.js, PostgreSQL, and Chart.js for visualizations.
Include mobile-responsive design.
```

**What you get:**
- Workout and exercise models
- Progress tracking with historical data
- Workout plan templates
- Social features (follow, compare)
- Analytics and charts
- Notification system
- Responsive mobile UI
- Full API with filtering and sorting

---

## Customer Support Portal

```
Build a customer support portal with:
- Customers can submit support tickets
- Tickets have priority levels and status tracking
- Support team can comment and update tickets
- Knowledge base with searchable articles
- Ticket search and filtering
- Email notifications for updates

Use Next.js, PostgreSQL, Prisma.
Include role-based access (Customer, Support Agent, Admin).
```

**What you get:**
- Ticket management system
- Multi-tier user roles with permissions
- Knowledge base with categories
- Email notification system
- Search functionality
- Status workflow (New → Assigned → In Progress → Resolved)
- Admin analytics dashboard
- Full CRUD APIs and tests

---

## Collaborative Notes App

```
Build a collaborative notes app where:
- Users can create shared note-taking spaces
- Invite other users to collaborate in real-time
- Notes support rich formatting and code blocks
- Version history and restore previous versions
- Search across all notes
- Organize notes by folders

Use WebSockets for real-time collaboration, PostgreSQL, and Prisma.
Include dark mode and mobile support.
```

**What you get:**
- Real-time collaborative editing
- Rich text editor integration
- Version history with rollback
- Shared workspace with permissions
- Full-text search API
- Folder organization
- Mobile app with sync
- Conflict resolution for concurrent edits

---

## How to Use These Prompts

1. **Choose a prompt** - Pick the application that matches your needs
2. **Copy the prompt** - Paste it into Cursor's chat
3. **Customize if needed** - Modify tech stack or features as desired
4. **Let it build** - Cursor will generate the complete application
5. **Review and test** - Check the code, run tests, and iterate

### Tips

- **Add constraints**: "Make it work offline" or "Optimize for mobile"
- **Change stack**: "Use Vue instead of React" or "Use Supabase instead of Prisma"
- **Scale it up**: "Add email notifications" or "Add real-time WebSocket updates"
- **Combine features**: Mix and match features from multiple prompts

---

## Advanced Patterns to Combine

### Add Authentication
```
Add NextAuth.js authentication with:
- Email/password signup
- Magic link login
- OAuth with GitHub and Google
```

### Add Real-time Updates
```
Add WebSocket support for real-time updates using Socket.io
```

### Add File Uploads
```
Add file upload support with AWS S3 or local storage
```

### Add Analytics
```
Add analytics tracking with Mixpanel or Amplitude
```

### Add Payments
```
Add Stripe payment integration for subscriptions
```

### Add Background Jobs
```
Add job queue with Bull for background tasks and email sending
```

---

## Notes

- All prompts assume a fresh Next.js 14 project
- Tech stack can be customized in your `.cursor/rules/imagine-builder.mdc`
- Agents will automatically coordinate across specialties
- Generated code includes tests and follows production patterns
- Start with a simple version, then layer on complexity

For more guidance on using agents, see [AGENTS.md](./AGENTS.md)
