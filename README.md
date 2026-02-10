# 💰 MERN Expense Tracker

A full-stack MERN (MongoDB, Express.js, React, Node.js) Expense Tracker application that allows users to securely track their income and expenses with a modern, responsive UI.

![Expense Tracker](https://via.placeholder.com/1200x600/0ea5e9/ffffff?text=Expense+Tracker+Screenshot)

## ✨ Features

### Core Functionality
- 📝 **Add, Edit, Delete** income and expense transactions
- 🏷️ **Categorize** transactions (Food, Rent, Travel, Salary, etc.)
- 📅 **Track** transactions by date
- 📊 **Dashboard** showing total income, total expenses, and current balance

### Authentication & Security
- 🔐 **JWT Authentication** for secure login/signup
- 🔒 **Password hashing** with bcrypt
- 🛡️ **Protected routes** for authenticated users

### Data Visualization
- 🥧 **Pie chart** for category-wise expenses
- 📊 **Bar chart** for monthly income vs expenses
- 📈 **Line chart** for spending trends over time

### Advanced Features
- 🔍 **Filter** transactions by date range, category, and type
- 🔎 **Search** transactions by description
- 💵 **Budget setting** with alerts when spending exceeds threshold
- 📥 **Export** transaction data as CSV or PDF
- 💡 **AI-based insights** for spending pattern analysis
- 🌍 **Multi-currency support** with real-time conversion (optional)

## 🚀 Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM library
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **express-validator** - Input validation
- **PDFKit** - PDF generation

### Frontend
- **React.js** - UI library
- **React Router** - Routing
- **Tailwind CSS** - Styling
- **Chart.js** - Data visualization
- **Framer Motion** - Animations
- **React Hot Toast** - Notifications
- **date-fns** - Date formatting

## 📁 Project Structure

```
expense-tracker/
├── backend/
│   ├── middleware/
│   │   └── auth.js          # Authentication middleware
│   ├── models/
│   │   ├── User.js          # User schema
│   │   ├── Transaction.js    # Transaction schema
│   │   └── Budget.js        # Budget schema
│   ├── routes/
│   │   ├── auth.js          # Authentication routes
│   │   ├── transactions.js   # Transaction routes
│   │   ├── budgets.js       # Budget routes
│   │   └── export.js        # Export routes
│   ├── .env.example          # Environment variables template
│   ├── package.json
│   └── server.js            # Main server file
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   └── Layout.js    # Main layout component
│   │   ├── context/
│   │   │   ├── AuthContext.js  # Authentication context
│   │   │   └── ThemeContext.js # Theme context
│   │   ├── pages/
│   │   │   ├── Dashboard.js    # Dashboard page
│   │   │   ├── Transactions.js # Transactions page
│   │   │   ├── Budgets.js      # Budgets page
│   │   │   ├── Insights.js     # Insights page
│   │   │   ├── Export.js       # Export page
│   │   │   ├── Settings.js     # Settings page
│   │   │   ├── Login.js        # Login page
│   │   │   └── Register.js     # Register page
│   │   ├── utils/
│   │   │   └── api.js         # API utilities
│   │   ├── App.js
│   │   ├── index.js
│   │   └── index.css
│   ├── package.json
│   └── tailwind.config.js
├── package.json              # Root package.json
└── README.md
```

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file based on `.env.example`:
```bash
cp .env.example .env
```

4. Update the `.env` file with your values:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/expense-tracker
JWT_SECRET=your_super_secret_jwt_key
JWT_EXPIRE=7d
```

5. Start the backend server:
```bash
npm run dev
```

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

### Run Both (Development)

From the root directory:
```bash
npm run install:all
npm run dev
```

## 📱 Screenshots

### Dashboard
![Dashboard](https://via.placeholder.com/800x500/f3f4f6/374151?text=Dashboard)

### Transactions
![Transactions](https://via.placeholder.com/800x500/f3f4f6/374151?text=Transactions)

### Budgets
![Budgets](https://via.placeholder.com/800x500/f3f4f6/374151?text=Budgets)

### Insights
![Insights](https://via.placeholder.com/800x500/f3f4f6/374151?text=Insights)

## 🔑 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/me` | Get current user |
| PUT | `/api/auth/updateprofile` | Update profile |
| PUT | `/api/auth/updatepassword` | Update password |

### Transactions
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/transactions` | Get all transactions |
| GET | `/api/transactions/summary` | Get dashboard summary |
| POST | `/api/transactions` | Create transaction |
| PUT | `/api/transactions/:id` | Update transaction |
| DELETE | `/api/transactions/:id` | Delete transaction |

### Budgets
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/budgets` | Get all budgets |
| GET | `/api/budgets/alerts` | Get budget alerts |
| POST | `/api/budgets` | Create budget |
| PUT | `/api/budgets/:id` | Update budget |
| DELETE | `/api/budgets/:id` | Delete budget |

### Export
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/export/csv` | Export as CSV |
| GET | `/api/export/pdf` | Export as PDF |
| GET | `/api/export/insights` | Get spending insights |

## 🎨 Color Palette

### Primary Colors
| Name | Hex | Usage |
|------|-----|-------|
| Primary 500 | `#0ea5e9` | Main brand color |
| Primary 600 | `#0284c7` | Hover state |
| Primary 100 | `#e0f2fe` | Light backgrounds |

### Semantic Colors
| Name | Hex | Usage |
|------|-----|-------|
| Success | `#22c55e` | Income, success states |
| Danger | `#ef4444` | Expenses, error states |
| Warning | `#f59e0b` | Alerts, warnings |

## 📱 Responsive Design

The application is fully responsive and works on:
- 📱 Mobile devices (320px+)
- 📱 Tablets (768px+)
- 💻 Desktops (1024px+)
- 🖥️ Large screens (1280px+)

## 🔒 Security Features

- JWT token-based authentication
- Password hashing with bcrypt
- Protected API routes
- Input validation and sanitization
- Secure HTTP headers
- CORS configuration

## ⚡ Performance Optimizations

- MongoDB indexing for fast queries
- Pagination for large datasets
- Lazy loading for routes
- Optimized database queries
- Efficient state management

## 🚀 Deployment

### Backend (Render/Heroku)
1. Push code to GitHub
2. Connect repository to platform
3. Set environment variables
4. Deploy

### Frontend (Vercel/Netlify)
1. Push code to GitHub
2. Connect repository
3. Set build command: `npm run build`
4. Set output directory: `build`
5. Add environment variable: `REACT_APP_API_URL`

### Database (MongoDB Atlas)
1. Create MongoDB Atlas account
2. Create cluster
3. Create database user
4. Whitelist IP addresses
5. Get connection string
6. Add to backend `.env`

## 📝 License

This project is licensed under the MIT License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📧 Support

For support, email karthik05399@gmail.com or open an issue.

---

Built with ❤️ using MERN Stack
