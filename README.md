# Wealth Management Dashboard

A modern, professional dashboard for fund management web applications inspired by leading fintech platforms like Robinhood, Vanguard, and Fidelity Investments.

## Features

### 🎨 Modern Design
- **Clean and Professional Interface**: Minimalist design emphasizing clarity and trust
- **Fintech Aesthetic**: Inspired by industry-leading platforms
- **Responsive Layout**: Fully responsive across desktop, tablet, and mobile devices
- **Light/Dark Mode**: Toggle between light and dark themes with persistent storage

### 📊 Dashboard Components

#### Summary Cards
- **Total Portfolio Value**: Real-time overview of your complete investment portfolio
- **Total Deposits**: Year-to-date deposits tracking
- **Total Withdrawals**: Year-to-date withdrawals tracking
- **Net Gain/Loss**: Overall profit/loss with percentage change indicators

#### Portfolio Performance Chart
- Interactive line chart showing portfolio value over time
- Time-based filtering: 1W, 1M, 3M, 1Y, ALL
- Hover tooltips with precise values and dates
- Smooth animations and transitions

#### Fund Allocation
- Doughnut chart showing investment distribution across:
  - Stocks (51%)
  - Commodities (31%)
  - Bonds (15%)
  - Cash (3%)
- Color-coded segments with legend
- Visual representation of asset allocation strategy

#### Asset Breakdown Table
- Comprehensive list of all investments
- Columns: Asset Name, Type, Invested, Current Value, Portfolio %, Profit/Loss
- **Sorting**: Click column headers to sort ascending/descending
- **Filtering**: Filter by asset name and type (Stock, Commodity, Bond)
- Color-coded profit/loss indicators

#### Recent Transactions
- Deposits, withdrawals, and asset transactions
- Columns: Date, Type, Asset, Amount, Status
- **Search**: Find transactions by asset name or type
- **Filtering**: Filter by transaction type
- **Pagination**: Navigate through transaction history
- Status badges for transaction completion state

#### Alerts & Notifications
- Deposit confirmations
- Portfolio milestone notifications
- Market volatility warnings
- Color-coded alert severity (success, info, warning)

### 🧭 Navigation
- **Sidebar Navigation**: Easy access to Dashboard, Portfolio, Transactions, Settings
- **Active State Indicators**: Visual feedback for current section
- **User Profile**: Quick access to account information
- **Responsive Mobile Menu**: Bottom navigation bar on mobile devices

## Getting Started

### Desktop Usage

1. **Open the Dashboard**
   - Open `index.html` in your web browser
   - The dashboard loads with sample data

2. **Navigate Sections**
   - Click sidebar items to switch between Dashboard, Portfolio, Transactions, and Settings
   - View relevant information for each section

3. **Interact with Data**
   - Click summary cards to explore details
   - Use time filter buttons on the performance chart
   - Sort tables by clicking column headers
   - Search and filter assets using the filter inputs
   - Paginate through transactions

4. **Toggle Theme**
   - Click the sun/moon icon in the header
   - Theme preference is saved in browser localStorage

### Mobile Usage

1. **Responsive Layout**: Dashboard automatically adapts to smaller screens
2. **Bottom Navigation**: Tap navigation items at the bottom of the screen
3. **Optimized Tables**: Compact table layout for mobile viewing
4. **Touch-Friendly**: Large touch targets for easy interaction

## Project Structure

```
/workspaces/webapp/
├── index.html          # Main HTML structure
├── styles.css          # Comprehensive styling with light/dark modes
├── script.js           # Interactive functionality and data management
└── README.md          # This file
```

## Technical Details

### Technologies Used
- **HTML5**: Semantic markup and structure
- **CSS3**: Modern styling with CSS variables and Grid/Flexbox
- **JavaScript (Vanilla)**: No dependencies except Chart.js
- **Chart.js 4.4.0**: Professional charts via CDN

### Design System

#### Color Palette
- **Primary**: #3B82F6 (Blue) - Action and primary elements
- **Secondary**: #10B981 (Green) - Success states
- **Warning**: #F59E0B (Amber) - Caution states
- **Danger**: #EF4444 (Red) - Error states
- **Info**: #0EA5E9 (Light Blue) - Information states

#### Typography
- System font stack for optimal readability
- Clear hierarchy with distinct font sizes and weights
- Accessible contrast ratios

#### Spacing & Layout
- Consistent spacing scale (xs, sm, md, lg, xl, 2xl)
- Grid-based layout system
- Flexible component sizing

### Data Management

The dashboard uses sample data for demonstration:
- **10 Sample Assets**: Stocks, commodities, bonds, and cash
- **15 Sample Transactions**: Deposits, withdrawals, buys, and sells
- **8-Week Portfolio History**: Historical performance data

All data is managed in `script.js` with the following structure:
```javascript
sampleAssets = [...]      // Asset holdings
sampleTransactions = [...] // Transaction history
portfolioData = {...}      // Historical performance
state = {...}              // Application state
```

### Responsive Breakpoints

- **Desktop**: 1200px+ (Full sidebar, expanded layout)
- **Tablet**: 768px - 1199px (Adjusted grid columns)
- **Mobile**: < 768px (Bottom navigation, single column)
- **Small Mobile**: < 480px (Compact layout, hidden elements)

## Features in Detail

### 1. Theme Management
- LocalStorage persistence
- Smooth transitions between light and dark modes
- Charts update colors dynamically

### 2. Chart Rendering
- Portfolio performance line chart with gradient fill
- Asset allocation doughnut chart
- Responsive chart containers
- Interactive tooltips with formatted data

### 3. Table Functionality
- **Sorting**: Multi-column sortable tables
- **Filtering**: Real-time search and type filtering
- **Pagination**: 10 items per page with navigation
- **Responsive**: Horizontal scroll on mobile

### 4. Accessibility
- Semantic HTML
- ARIA labels on interactive elements
- Color contrast compliance
- Keyboard navigation support
- Focus states on all interactive elements

## Customization Guide

### Updating Sample Data
Edit the data arrays in `script.js`:
```javascript
const sampleAssets = [...]        // Modify asset list
const sampleTransactions = [...]   // Modify transaction list
const portfolioData = {...}        // Update historical data
```

### Changing Colors
Modify CSS custom properties in `styles.css`:
```css
:root {
    --primary-color: #3b82f6;      /* Change primary color */
    --secondary-color: #10b981;    /* Change secondary color */
    /* ... other colors ... */
}
```

### Adjusting Layout
Modify grid templates and spacing:
```css
.summary-cards {
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: var(--spacing-lg);
}
```

### Adding New Sections
1. Add section in HTML structure
2. Create corresponding CSS styles
3. Add navigation link
4. Implement section logic in JavaScript

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Optimizations

- CSS Grid and Flexbox for efficient layouts
- Minimal JavaScript dependencies (Chart.js only)
- Debounced search and filter operations
- Efficient DOM updates
- SVG icons for sharp rendering at all sizes

## Future Enhancements

Potential features for expansion:
- **Real Data Integration**: Connect to financial data APIs
- **Advanced Analytics**: Additional chart types and metrics
- **Watchlist Feature**: Track specific assets
- **Portfolio Rebalancing**: Automated allocation suggestions
- **Tax Reports**: Capital gains and loss reporting
- **Export Functionality**: Download reports as PDF/CSV
- **User Authentication**: Login and multi-user support
- **Historical Comparisons**: Year-over-year analysis
- **Custom Alerts**: User-defined price notifications
- **Mobile App**: Native iOS/Android applications

## Accessibility

The dashboard follows WCAG 2.1 AA standards:
- Semantic HTML structure
- Proper heading hierarchy
- Color contrast ratios ≥ 4.5:1
- Focus visible states
- Keyboard navigation support
- ARIA labels for icons
- Alt text for images

## Best Practices Implemented

✅ **Responsive Design**: Mobile-first approach
✅ **CSS Organization**: Variables, clear structure
✅ **Performance**: Optimized rendering and animations
✅ **Accessibility**: WCAG compliant
✅ **Code Quality**: Clean, well-commented code
✅ **User Experience**: Intuitive navigation, clear feedback
✅ **Dark Mode**: System and manual theme switching
✅ **Data Integrity**: Proper data filtering and sorting

## License

This project is provided as-is for educational and commercial use.

## Support

For questions or suggestions about the dashboard design, please refer to the inline code comments and documentation.

---

**Created**: March 5, 2026
**Version**: 1.0.0
**Status**: Production Ready
