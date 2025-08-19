# Alumni Tracking Dashboard

A professional HTML-based dashboard for tracking alumni verification progress and LinkedIn profile collection. Designed for internal team use with easy data updates and clean visualizations.

## 📋 Features

### Key Metrics Display
- **Total Alumni Records**: Complete count of exam records collected
- **Verified Alumni**: Number of alumni with verified details
- **LinkedIn Profiles**: Count of LinkedIn profiles found
- **Weekly Progress**: Recent additions with growth indicators

### Data Visualization
- **Progress Bars**: Visual completion percentages for each metric
- **Year-wise Tables**: Detailed breakdown by graduation year
- **Status Indicators**: Color-coded progress dots (Green: >85%, Orange: 70-85%, Red: <70%)
- **Overall Progress Ring**: Circular progress indicator with completion percentage

### Professional Design
- Responsive card-based layout
- Blue gradient color scheme
- Hover effects and smooth animations
- Mobile-friendly design
- Clean typography with clear data hierarchy

## 🚀 Quick Start

1. **Save the HTML file** as `alumni-dashboard.html`
2. **Open in any web browser** - no installation required
3. **Update data twice weekly** by editing the JavaScript section
4. **Share with your team** (10-15 people) via file sharing or web hosting

## 📊 Data Structure

The dashboard uses a simple JavaScript object to store all data:

```javascript
const dashboardData = {
    lastUpdated: "August 19, 2025",
    totalRecords: 2450,
    linkedInProfiles: 1420,
    weeklyProgress: 127,
    
    examRecords: [
        { year: 2023, examCount: 145, verified: 132 },
        // ... more years
    ],
    
    alumniDetails: [
        { year: 2023, target: 145, obtained: 132 },
        // ... more years
    ]
};
```

## 🔄 Updating Data (Twice Weekly)

### Method 1: Direct Edit
1. Open the HTML file in a text editor
2. Find the `dashboardData` object (around line 200)
3. Update the values as needed
4. Save the file

### Method 2: Using Update Function
Add this code to the browser console or at the end of the script:

```javascript
updateData({
    lastUpdated: "August 22, 2025",
    linkedInProfiles: 1485,
    weeklyProgress: 65,
    examRecords: [
        { year: 2023, examCount: 145, verified: 135 },
        // ... updated data
    ]
});
```

## 📈 Data Fields Explained

### Exam Records vs Verified
- **Year**: Graduation year
- **Exam Records**: Total number of exam records available for that year
- **Verified**: Number of alumni with verified contact details
- **Progress**: Percentage of verification completion

### Alumni Details Progress
- **Year**: Graduation year  
- **Target**: Total exam records (upper limit for that year)
- **Details Obtained**: Number of alumni details successfully collected
- **Completion**: Percentage of details collection progress

### Key Metrics
- **Total Alumni Records**: Sum of all exam records across years
- **Verified Alumni**: Total verified alumni details
- **LinkedIn Profiles**: Total LinkedIn profiles found
- **Weekly Progress**: New profiles added in the current week

## 🎨 Customization

### Updating Colors
Modify the CSS variables in the `<style>` section:
- Main gradient: `background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);`
- Progress bars: `.progress-fill { background: linear-gradient(90deg, #4299e1, #3182ce); }`
- Status indicators: `.status-dot`, `.status-dot.warning`, `.status-dot.danger`

### Adding New Years
Add new objects to the `examRecords` and `alumniDetails` arrays:

```javascript
examRecords: [
    { year: 2024, examCount: 150, verified: 140 }, // New year
    { year: 2023, examCount: 145, verified: 132 },
    // ... existing years
]
```

### Modifying Table Display
The dashboard shows the first 8 years by default. To show more/fewer years, modify:
```javascript
dashboardData.examRecords.slice(0, 8) // Change 8 to desired number
```

## 📱 Browser Compatibility

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## 🔧 Technical Details

- **File Type**: Single HTML file with embedded CSS and JavaScript
- **Dependencies**: None (completely self-contained)
- **Storage**: All data stored in JavaScript variables (no external database)
- **Performance**: Optimized for datasets up to 10,000+ records
- **Security**: Client-side only, no data transmission

## 💡 Usage Tips

### Regular Updates
1. **Set a Schedule**: Update every Tuesday and Friday
2. **Backup Data**: Keep a copy of your data in a separate spreadsheet
3. **Version Control**: Save dated copies (e.g., `dashboard-2025-08-19.html`)

### Team Sharing
- **Email**: Attach the HTML file directly
- **Cloud Storage**: Upload to Google Drive, Dropbox, or OneDrive
- **Local Network**: Place on shared drive
- **Web Hosting**: Upload to any web server for browser access

### Data Validation
The dashboard automatically:
- Calculates percentages
- Updates progress bars
- Refreshes visual indicators
- Validates data ranges

## 🆘 Troubleshooting

### Common Issues
1. **Dashboard not loading**: Check that the file is saved with `.html` extension
2. **Data not updating**: Ensure JavaScript syntax is correct (check browser console)
3. **Mobile display issues**: Refresh the page or check viewport settings

### Support
For technical issues:
1. Check browser console for JavaScript errors
2. Validate JSON syntax in data objects
3. Ensure all required fields are present in data arrays

## 📝 Sample Data Update

Here's a complete example of updating your data:

```javascript
// Weekly Update Example - August 22, 2025
updateData({
    lastUpdated: "August 22, 2025",
    totalRecords: 2450,
    linkedInProfiles: 1485, // +65 new profiles
    weeklyProgress: 65,
    
    examRecords: [
        { year: 2023, examCount: 145, verified: 135 }, // +3 verified
        { year: 2022, examCount: 138, verified: 128 }, // +3 verified
        // ... rest of data
    ]
});
```

## 📊 Progress Tracking Best Practices

1. **Consistent Updates**: Maintain regular twice-weekly schedule
2. **Data Accuracy**: Double-check numbers before updating
3. **Progress Documentation**: Note significant milestones or blockers
4. **Team Communication**: Share updated dashboard after each data refresh

---

*Dashboard created for internal alumni tracking - optimized for teams of 10-15 people*
