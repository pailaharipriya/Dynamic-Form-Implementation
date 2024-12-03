# Dynamic Form Builder

A modern, responsive React application that demonstrates dynamic form generation and management with TypeScript and Tailwind CSS.

## Features

- 🔄 Dynamic form generation based on configuration
- ✨ Real-time form validation
- 📊 Progress tracking with visual feedback
- 📱 Fully responsive design
- 🎯 Interactive data table with edit and delete capabilities
- 🔔 Toast notifications for user feedback
- 🎨 Modern UI with Tailwind CSS
- 🏷️ Type-safe with TypeScript

## Available Form Types

1. **User Information**
   - First Name
   - Last Name
   - Age

2. **Address Information**
   - Street
   - City
   - State (dropdown)
   - Zip Code

3. **Payment Information**
   - Card Number
   - Expiry Date
   - CVV
   - Cardholder Name

## Tech Stack

- React 18
- TypeScript
- Tailwind CSS
- Vite
- Lucide React (for icons)

## Project Structure

```
src/
├── components/          # React components
│   ├── DataTable.tsx   # Table for displaying form entries
│   ├── FormField.tsx   # Dynamic form field component
│   ├── ProgressBar.tsx # Progress indicator
│   └── Toast.tsx       # Notification component
├── data/
│   └── mockApi.ts      # Simulated API responses
├── types/
│   └── form.ts         # TypeScript interfaces
├── App.tsx             # Main application component
└── main.tsx           # Application entry point
```

## Getting Started

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

3. Build for production:
   ```bash
   npm run build
   ```

## Features in Detail

### Dynamic Form Generation
Forms are generated dynamically based on configuration received from the mock API. Each form type has its own set of fields with specific validation rules.

### Form Validation
- Required field validation
- Real-time error feedback
- Visual indicators for required fields

### Progress Tracking
A progress bar indicates how much of the required fields have been completed, updating in real-time as users fill out the form.

### Data Management
- View submitted entries in a table format
- Edit existing entries
- Delete entries
- Sortable columns

### Notifications
Toast notifications provide feedback for:
- Successful form submission
- Validation errors
- Edit mode activation
- Entry deletion

## Component Usage

### FormField
```tsx
<FormField
  field={fieldConfig}
  value={fieldValue}
  error={errorMessage}
  onChange={handleChange}
/>
```

### ProgressBar
```tsx
<ProgressBar progress={percentageComplete} />
```

### DataTable
```tsx
<DataTable
  entries={formEntries}
  onEdit={handleEdit}
  onDelete={handleDelete}
/>
```

### Toast
```tsx
<Toast
  message="Operation successful!"
  type="success"
  onClose={handleClose}
/>
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
