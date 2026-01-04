# Component Patterns

Reusable, minimalistic component patterns for web applications using Tailwind CSS and JavaScript.

## Buttons

### Button Variants

```jsx
// components/ui/button.tsx
const buttonVariants = {
  primary: "bg-blue-600 text-white hover:bg-blue-700 focus:ring-blue-500",
  secondary: "bg-slate-100 text-slate-700 hover:bg-slate-200 focus:ring-slate-500 dark:bg-slate-800 dark:text-slate-200 dark:hover:bg-slate-700",
  ghost: "text-slate-600 hover:bg-slate-100 hover:text-slate-900 focus:ring-slate-500 dark:text-slate-400 dark:hover:bg-slate-800 dark:hover:text-slate-100",
  danger: "bg-red-600 text-white hover:bg-red-700 focus:ring-red-500",
  outline: "border border-slate-300 text-slate-700 hover:bg-slate-50 focus:ring-slate-500 dark:border-slate-600 dark:text-slate-300 dark:hover:bg-slate-800",
};

const buttonSizes = {
  sm: "px-3 py-1.5 text-sm",
  md: "px-4 py-2 text-sm",
  lg: "px-6 py-3 text-base",
};

export function Button({ variant = "primary", size = "md", children, ...props }) {
  return (
    <button
      className={`
        inline-flex items-center justify-center font-medium rounded-lg
        transition-colors focus:outline-none focus:ring-2 focus:ring-offset-2
        disabled:opacity-50 disabled:pointer-events-none
        ${buttonVariants[variant]}
        ${buttonSizes[size]}
      `}
      {...props}
    >
      {children}
    </button>
  );
}
```

### Icon Button

```jsx
export function IconButton({ children, label, size = "md", ...props }) {
  const sizes = {
    sm: "w-8 h-8",
    md: "w-10 h-10",
    lg: "w-12 h-12",
  };

  return (
    <button
      className={`
        inline-flex items-center justify-center rounded-lg
        text-slate-600 hover:text-slate-900 hover:bg-slate-100
        transition-colors focus:outline-none focus:ring-2 focus:ring-slate-500 focus:ring-offset-2
        dark:text-slate-400 dark:hover:text-slate-100 dark:hover:bg-slate-800
        ${sizes[size]}
      `}
      aria-label={label}
      {...props}
    >
      {children}
    </button>
  );
}
```

### Button Group

```jsx
export function ButtonGroup({ children }) {
  return (
    <div className="inline-flex rounded-lg overflow-hidden border border-slate-200 dark:border-slate-700">
      {children}
    </div>
  );
}

export function ButtonGroupItem({ active, children, ...props }) {
  return (
    <button
      className={`
        px-4 py-2 text-sm font-medium border-r last:border-r-0 border-slate-200
        transition-colors focus:outline-none focus:z-10 focus:ring-2 focus:ring-blue-500
        dark:border-slate-700
        ${active
          ? "bg-blue-600 text-white"
          : "bg-white text-slate-700 hover:bg-slate-50 dark:bg-slate-800 dark:text-slate-300 dark:hover:bg-slate-700"
        }
      `}
      {...props}
    >
      {children}
    </button>
  );
}
```

## Cards

### Basic Card

```jsx
export function Card({ children, className = "" }) {
  return (
    <div className={`
      p-6 bg-white rounded-xl border border-slate-200
      dark:bg-slate-800 dark:border-slate-700
      ${className}
    `}>
      {children}
    </div>
  );
}

export function CardHeader({ children }) {
  return <div className="mb-4">{children}</div>;
}

export function CardTitle({ children }) {
  return <h3 className="text-lg font-semibold text-slate-900 dark:text-white">{children}</h3>;
}

export function CardDescription({ children }) {
  return <p className="mt-1 text-sm text-slate-500 dark:text-slate-400">{children}</p>;
}

export function CardContent({ children }) {
  return <div className="text-slate-600 dark:text-slate-300">{children}</div>;
}

export function CardFooter({ children }) {
  return <div className="mt-4 pt-4 border-t border-slate-200 dark:border-slate-700">{children}</div>;
}
```

### Interactive Card

```jsx
export function InteractiveCard({ href, children }) {
  const Component = href ? 'a' : 'div';

  return (
    <Component
      href={href}
      className={`
        block p-6 bg-white rounded-xl border border-slate-200
        hover:border-slate-300 hover:shadow-sm
        transition-all cursor-pointer
        dark:bg-slate-800 dark:border-slate-700 dark:hover:border-slate-600
      `}
    >
      {children}
    </Component>
  );
}
```

### Stat Card

```jsx
export function StatCard({ icon, label, value, change, changeType }) {
  return (
    <div className="p-6 bg-white rounded-xl border border-slate-200 dark:bg-slate-800 dark:border-slate-700">
      <div className="flex items-center justify-between">
        <div className="p-2 bg-slate-100 rounded-lg dark:bg-slate-700">
          {icon}
        </div>
        {change && (
          <span className={`text-sm font-medium ${
            changeType === 'positive' ? 'text-green-600' : 'text-red-600'
          }`}>
            {change}
          </span>
        )}
      </div>
      <p className="mt-4 text-2xl font-bold text-slate-900 dark:text-white">{value}</p>
      <p className="mt-1 text-sm text-slate-500 dark:text-slate-400">{label}</p>
    </div>
  );
}
```

## Form Elements

### Input

```jsx
export function Input({ label, error, hint, ...props }) {
  return (
    <div>
      {label && (
        <label className="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-1">
          {label}
        </label>
      )}
      <input
        className={`
          block w-full px-3 py-2 rounded-lg
          bg-white border text-slate-900 placeholder-slate-400
          focus:outline-none focus:ring-2 focus:border-transparent
          dark:bg-slate-800 dark:text-white dark:placeholder-slate-500
          ${error
            ? "border-red-500 focus:ring-red-500"
            : "border-slate-300 focus:ring-blue-500 dark:border-slate-600"
          }
        `}
        {...props}
      />
      {hint && !error && (
        <p className="mt-1 text-sm text-slate-500">{hint}</p>
      )}
      {error && (
        <p className="mt-1 text-sm text-red-600">{error}</p>
      )}
    </div>
  );
}
```

### Input with Icon

```jsx
export function InputWithIcon({ icon, iconPosition = "left", ...props }) {
  return (
    <div className="relative">
      <div className={`
        absolute inset-y-0 flex items-center pointer-events-none text-slate-400
        ${iconPosition === "left" ? "left-0 pl-3" : "right-0 pr-3"}
      `}>
        {icon}
      </div>
      <input
        className={`
          block w-full py-2 rounded-lg
          bg-white border border-slate-300 text-slate-900 placeholder-slate-400
          focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent
          dark:bg-slate-800 dark:border-slate-600 dark:text-white
          ${iconPosition === "left" ? "pl-10 pr-3" : "pl-3 pr-10"}
        `}
        {...props}
      />
    </div>
  );
}
```

### Select

```jsx
export function Select({ label, options, ...props }) {
  return (
    <div>
      {label && (
        <label className="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-1">
          {label}
        </label>
      )}
      <select
        className="
          block w-full px-3 py-2 rounded-lg appearance-none
          bg-white border border-slate-300 text-slate-900
          focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent
          dark:bg-slate-800 dark:border-slate-600 dark:text-white
        "
        {...props}
      >
        {options.map(option => (
          <option key={option.value} value={option.value}>
            {option.label}
          </option>
        ))}
      </select>
    </div>
  );
}
```

### Checkbox

```jsx
export function Checkbox({ label, ...props }) {
  return (
    <label className="flex items-center gap-3 cursor-pointer">
      <input
        type="checkbox"
        className="
          w-4 h-4 rounded border-slate-300
          text-blue-600 focus:ring-blue-500 focus:ring-offset-0
          dark:border-slate-600 dark:bg-slate-800
        "
        {...props}
      />
      <span className="text-sm text-slate-700 dark:text-slate-300">{label}</span>
    </label>
  );
}
```

### Toggle Switch

```jsx
export function Toggle({ checked, onChange, label }) {
  return (
    <label className="flex items-center gap-3 cursor-pointer">
      <button
        role="switch"
        aria-checked={checked}
        onClick={() => onChange(!checked)}
        className={`
          relative inline-flex h-6 w-11 shrink-0 rounded-full
          transition-colors focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2
          ${checked ? "bg-blue-600" : "bg-slate-200 dark:bg-slate-700"}
        `}
      >
        <span
          className={`
            inline-block h-5 w-5 rounded-full bg-white shadow
            transform transition-transform
            ${checked ? "translate-x-5" : "translate-x-0.5"}
            mt-0.5
          `}
        />
      </button>
      {label && <span className="text-sm text-slate-700 dark:text-slate-300">{label}</span>}
    </label>
  );
}
```

## Navigation

### Tabs

```jsx
export function Tabs({ tabs, activeTab, onChange }) {
  return (
    <div className="border-b border-slate-200 dark:border-slate-700">
      <nav className="flex gap-8" aria-label="Tabs">
        {tabs.map(tab => (
          <button
            key={tab.id}
            onClick={() => onChange(tab.id)}
            className={`
              py-4 text-sm font-medium border-b-2 -mb-px
              transition-colors focus:outline-none
              ${activeTab === tab.id
                ? "border-blue-600 text-blue-600"
                : "border-transparent text-slate-500 hover:text-slate-700 hover:border-slate-300 dark:text-slate-400 dark:hover:text-slate-300"
              }
            `}
          >
            {tab.label}
          </button>
        ))}
      </nav>
    </div>
  );
}
```

### Breadcrumbs

```jsx
export function Breadcrumbs({ items }) {
  return (
    <nav aria-label="Breadcrumb">
      <ol className="flex items-center gap-2 text-sm">
        {items.map((item, index) => (
          <li key={item.href} className="flex items-center gap-2">
            {index > 0 && (
              <svg className="w-4 h-4 text-slate-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2">
                <polyline points="9 18 15 12 9 6"/>
              </svg>
            )}
            {index === items.length - 1 ? (
              <span className="text-slate-900 font-medium dark:text-white">{item.label}</span>
            ) : (
              <a href={item.href} className="text-slate-500 hover:text-slate-700 dark:text-slate-400 dark:hover:text-slate-300">
                {item.label}
              </a>
            )}
          </li>
        ))}
      </ol>
    </nav>
  );
}
```

### Pagination

```jsx
export function Pagination({ currentPage, totalPages, onPageChange }) {
  const pages = Array.from({ length: totalPages }, (_, i) => i + 1);

  return (
    <nav className="flex items-center gap-1" aria-label="Pagination">
      <button
        onClick={() => onPageChange(currentPage - 1)}
        disabled={currentPage === 1}
        className="p-2 rounded-lg text-slate-600 hover:bg-slate-100 disabled:opacity-50 disabled:pointer-events-none dark:text-slate-400 dark:hover:bg-slate-800"
      >
        <svg className="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2">
          <polyline points="15 18 9 12 15 6"/>
        </svg>
      </button>

      {pages.map(page => (
        <button
          key={page}
          onClick={() => onPageChange(page)}
          className={`
            w-10 h-10 rounded-lg text-sm font-medium transition-colors
            ${page === currentPage
              ? "bg-blue-600 text-white"
              : "text-slate-600 hover:bg-slate-100 dark:text-slate-400 dark:hover:bg-slate-800"
            }
          `}
        >
          {page}
        </button>
      ))}

      <button
        onClick={() => onPageChange(currentPage + 1)}
        disabled={currentPage === totalPages}
        className="p-2 rounded-lg text-slate-600 hover:bg-slate-100 disabled:opacity-50 disabled:pointer-events-none dark:text-slate-400 dark:hover:bg-slate-800"
      >
        <svg className="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2">
          <polyline points="9 18 15 12 9 6"/>
        </svg>
      </button>
    </nav>
  );
}
```

## Feedback

### Alert

```jsx
const alertVariants = {
  info: "bg-blue-50 border-blue-200 text-blue-800 dark:bg-blue-900/20 dark:border-blue-800 dark:text-blue-300",
  success: "bg-green-50 border-green-200 text-green-800 dark:bg-green-900/20 dark:border-green-800 dark:text-green-300",
  warning: "bg-amber-50 border-amber-200 text-amber-800 dark:bg-amber-900/20 dark:border-amber-800 dark:text-amber-300",
  error: "bg-red-50 border-red-200 text-red-800 dark:bg-red-900/20 dark:border-red-800 dark:text-red-300",
};

export function Alert({ variant = "info", title, children }) {
  return (
    <div className={`p-4 rounded-lg border ${alertVariants[variant]}`} role="alert">
      {title && <p className="font-medium mb-1">{title}</p>}
      <p className="text-sm">{children}</p>
    </div>
  );
}
```

### Badge

```jsx
const badgeVariants = {
  default: "bg-slate-100 text-slate-700 dark:bg-slate-700 dark:text-slate-300",
  primary: "bg-blue-100 text-blue-700 dark:bg-blue-900/30 dark:text-blue-300",
  success: "bg-green-100 text-green-700 dark:bg-green-900/30 dark:text-green-300",
  warning: "bg-amber-100 text-amber-700 dark:bg-amber-900/30 dark:text-amber-300",
  error: "bg-red-100 text-red-700 dark:bg-red-900/30 dark:text-red-300",
};

export function Badge({ variant = "default", children }) {
  return (
    <span className={`
      inline-flex items-center px-2 py-0.5 rounded-full text-xs font-medium
      ${badgeVariants[variant]}
    `}>
      {children}
    </span>
  );
}
```

### Toast / Notification

```jsx
export function Toast({ message, type = "info", onClose }) {
  const icons = {
    info: <InfoIcon className="w-5 h-5 text-blue-500" />,
    success: <CheckCircleIcon className="w-5 h-5 text-green-500" />,
    warning: <AlertIcon className="w-5 h-5 text-amber-500" />,
    error: <XCircleIcon className="w-5 h-5 text-red-500" />,
  };

  return (
    <div className="
      flex items-center gap-3 p-4 bg-white rounded-lg shadow-lg border border-slate-200
      dark:bg-slate-800 dark:border-slate-700
    ">
      {icons[type]}
      <p className="text-sm text-slate-700 dark:text-slate-300">{message}</p>
      <button
        onClick={onClose}
        className="ml-auto p-1 text-slate-400 hover:text-slate-600 dark:hover:text-slate-200"
      >
        <XIcon className="w-4 h-4" />
      </button>
    </div>
  );
}
```

### Progress Bar

```jsx
export function ProgressBar({ value, max = 100, label }) {
  const percentage = (value / max) * 100;

  return (
    <div>
      {label && (
        <div className="flex justify-between mb-1">
          <span className="text-sm text-slate-700 dark:text-slate-300">{label}</span>
          <span className="text-sm text-slate-500">{percentage.toFixed(0)}%</span>
        </div>
      )}
      <div className="h-2 bg-slate-200 rounded-full overflow-hidden dark:bg-slate-700">
        <div
          className="h-full bg-blue-600 rounded-full transition-all"
          style={{ width: `${percentage}%` }}
        />
      </div>
    </div>
  );
}
```

## Layout

### Container

```jsx
export function Container({ children, size = "default" }) {
  const sizes = {
    sm: "max-w-3xl",
    default: "max-w-7xl",
    lg: "max-w-screen-2xl",
    full: "max-w-full",
  };

  return (
    <div className={`mx-auto px-4 sm:px-6 lg:px-8 ${sizes[size]}`}>
      {children}
    </div>
  );
}
```

### Section

```jsx
export function Section({ children, className = "" }) {
  return (
    <section className={`py-16 md:py-24 ${className}`}>
      {children}
    </section>
  );
}
```

### Divider

```jsx
export function Divider({ label }) {
  if (label) {
    return (
      <div className="flex items-center gap-4">
        <div className="flex-1 h-px bg-slate-200 dark:bg-slate-700" />
        <span className="text-sm text-slate-500">{label}</span>
        <div className="flex-1 h-px bg-slate-200 dark:bg-slate-700" />
      </div>
    );
  }

  return <hr className="border-slate-200 dark:border-slate-700" />;
}
```

## Loading States

### Spinner

```jsx
export function Spinner({ size = "md" }) {
  const sizes = {
    sm: "w-4 h-4",
    md: "w-6 h-6",
    lg: "w-8 h-8",
  };

  return (
    <svg
      className={`animate-spin text-blue-600 ${sizes[size]}`}
      viewBox="0 0 24 24"
      fill="none"
    >
      <circle
        className="opacity-25"
        cx="12"
        cy="12"
        r="10"
        stroke="currentColor"
        strokeWidth="4"
      />
      <path
        className="opacity-75"
        fill="currentColor"
        d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"
      />
    </svg>
  );
}
```

### Skeleton

```jsx
export function Skeleton({ className = "" }) {
  return (
    <div className={`animate-pulse bg-slate-200 rounded dark:bg-slate-700 ${className}`} />
  );
}

// Usage examples
<Skeleton className="h-4 w-3/4" />        // Text line
<Skeleton className="h-10 w-full" />      // Input
<Skeleton className="h-40 w-full" />      // Card
<Skeleton className="h-10 w-10 rounded-full" />  // Avatar
```

### Loading Button

```jsx
export function LoadingButton({ loading, children, ...props }) {
  return (
    <Button disabled={loading} {...props}>
      {loading ? (
        <>
          <Spinner size="sm" />
          <span className="ml-2">Loading...</span>
        </>
      ) : (
        children
      )}
    </Button>
  );
}
```

## Empty States

### Empty State

```jsx
export function EmptyState({ icon, title, description, action }) {
  return (
    <div className="flex flex-col items-center justify-center py-12 text-center">
      <div className="p-3 bg-slate-100 rounded-full dark:bg-slate-800">
        {icon}
      </div>
      <h3 className="mt-4 text-lg font-medium text-slate-900 dark:text-white">
        {title}
      </h3>
      <p className="mt-2 text-sm text-slate-500 max-w-sm">
        {description}
      </p>
      {action && (
        <div className="mt-6">
          {action}
        </div>
      )}
    </div>
  );
}
```
