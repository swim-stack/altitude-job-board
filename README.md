# Altitude Exhibits — Job Board

A modern, responsive job management dashboard for Altitude Exhibits. Track exhibition prep work, manage tasks, and maintain contact information in one centralized platform.

**Live Demo:** https://altitude-job-board.vercel.app

---

## Features

### 📊 Dashboard (Preps Tab)
- **Real-time statistics** showing total jobs, in-progress, pending, and completed counts
- **Advanced filtering** by status, project manager, and city
- **Full-text search** across jobs, clients, and shows
- **Sortable table** with all job details
- **One-click job creation** with modal form
- **Inline status updates** for quick workflow management

### ✅ Task Management (Tasks Tab)
- View all tasks across projects
- Filter by status and priority levels (High, Moderate, Low)
- Track task descriptions, assignments, and deadlines
- Category-based organization

### 👥 Contact Management (Contacts Tab)
- Searchable contact directory
- Grid-based contact cards with role information
- Quick access to contact details and communication info

### 🔐 Authentication
- Google Sign-In integration
- Secure session management
- User profile display with avatar

---

## Tech Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Authentication:** Google OAuth 2.0
- **Styling:** Custom CSS with dark theme and responsive design
- **Design System:** Custom component library with Bebas Neue, DM Sans, and DM Mono fonts

---

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Google OAuth credentials (for local development)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/swim-stack/altitude-job-board.git
   cd altitude-job-board
   ```

2. **Set up Google OAuth**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new OAuth 2.0 application
   - Add your local domain and deployed domain to authorized origins
   - Replace the `CLIENT_ID` in `index.html` with your credentials

3. **Serve locally**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

4. **Open in browser**
   ```
   http://localhost:8000
   ```

---

## File Structure

```
altitude-job-board/
├── index.html          # Main application file (HTML + CSS + JS)
├── README.md           # Project documentation
└── .gitignore          # Git ignore rules
```

---

## Key Components

### Authentication Flow
- Users sign in with Google OAuth
- Session tokens are validated client-side
- User profile information (name, email, avatar) is displayed in header

### Data Management
- Job data structure includes: Project ID, Status, Client, Show, Exhibitor, City, PM, Dates, Notes
- Real-time filtering and sorting of job records
- Modal-based job creation and editing

### UI/UX Highlights
- Dark mode theme with red accent color (#E1251B)
- Smooth animations and transitions
- Mobile-responsive design (2-column stats on tablets, 1-column on mobile)
- Toast notifications for user feedback
- Loading states with spinners

---

## Customization

### Color Scheme
Edit the CSS variables in the `<style>` section of `index.html`:
```css
:root {
  --red: #E1251B;
  --black: #0a0a0a;
  --surface: #111111;
  /* ... more variables ... */
}
```

### Font Family
- Display: Bebas Neue
- Body: DM Sans
- Mono: DM Mono

---

## Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Vercel will automatically deploy on every push
4. Update your Google OAuth redirect URIs in Google Cloud Console

### Other Platforms
This is a static HTML file, so it can be deployed to:
- GitHub Pages
- Netlify
- AWS S3 + CloudFront
- Traditional web servers

---

## Security Considerations

- ⚠️ **Google OAuth Credentials:** Keep your CLIENT_ID and client secrets secure. Never commit sensitive credentials to version control.
- **HTTPS Only:** Always use HTTPS in production for authentication flows
- **CORS:** Configure appropriate CORS headers for your backend API
- **Input Validation:** Validate all user inputs before submission

---

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

---

## Contributing

1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

---

## License

This project is proprietary to Altitude Exhibits.

---

## Support

For issues, questions, or feature requests, please contact the development team.

---

**Last Updated:** April 26, 2026
