# 💰 Expense Tracker App

A simple yet powerful **Flutter Expense Tracker App** that allows users to record, view, and analyze daily expenses. The app provides both a **list-based interface** for managing entries and a **chart-based interface** for visualizing spending patterns by category.

---

## ✨ Features

- ➕ **Add New Expenses**  
  - Input expense title, amount, date, and category (e.g., Food, Travel, Leisure, Work).  
  - Modal bottom sheet for smooth user input.  

- 📋 **Expense List**  
  - Scrollable list of all expenses.  
  - Each entry displays title, amount, date, and category icon.  
  - Swipe-to-delete with **undo option** via `SnackBar`.  

- 🗑️ **Delete and Undo**  
  - Expenses can be deleted with a single action.  
  - Deleted items can be restored with an **undo button**.  

- 📊 **Interactive Chart**  
  - Weekly bar chart showing category-based spending distribution.  
  - Custom `Chart` and `ChartBar` widgets built from scratch.  
  - Dynamic scaling to highlight highest spending categories.  

- 📱 **Responsive UI**  
  - Adapts to different screen sizes and orientations.  
  - Built with Flutter’s flexible widget tree and responsive layouts.  

---

## 📂 Project Structure

```
lib/
│── main.dart            # Entry point of the app
│── expenses.dart        # Main expenses screen with chart and list
│── new_expense.dart     # Form to add new expenses
│── expense.dart         # Expense model (title, amount, date, category)
│── expenses_item.dart   # Single expense item UI
│── expenses_list.dart   # List view of all expenses
│── chart.dart           # Chart widget summarizing expenses
│── chart_bar.dart       # Bar widget for chart visualization
```

---

## 🏗 Architecture & Design

- **State Management**:  
  - The app uses **`StatefulWidget`** for managing expenses in memory.  
  - Expenses are stored in a local list (`_registeredExpenses`) inside `expenses.dart`.  

- **Data Model**:  
  - `Expense` class defines:  
    ```dart
    class Expense {
      final String title;
      final double amount;
      final DateTime date;
      final Category category;
    }
    ```  
  - Categories are represented by an enum (`Category.food`, `Category.travel`, `Category.leisure`, `Category.work`).  

- **User Interface**:  
  - Clean **Material Design** UI.  
  - **BottomSheet** for adding new expenses.  
  - **ListTile**-based expense items with category icons.  

- **Charts**:  
  - `Chart` aggregates expenses by week and category.  
  - `ChartBar` renders each bar with proportional height relative to max spending.  

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/expense-tracker-app.git
cd expense-tracker-app
```

### 2. Install dependencies
```bash
flutter pub get
```

### 3. Run the app
```bash
flutter run
```

---

## 🛠 Built With

- [Flutter](https://flutter.dev/) – Cross-platform UI toolkit  
- [Dart](https://dart.dev/) – Programming language  
- [Material Design](https://m3.material.io/) – UI principles  

---

## 📊 Example Workflow

1. Launch the app → View expense list and chart.  
2. Tap **“+” button** → Add new expense with details.  
3. Expense appears in the list and chart updates automatically.  
4. Swipe left to delete an expense → Option to **undo** via Snackbar.  
5. Check weekly chart → See category distribution of spending.  

---

## 🔮 Future Improvements

- 💾 **Persistent Storage**: Save expenses to local database (e.g., `sqflite` or Hive).  
- ☁️ **Cloud Sync**: Enable syncing across devices using Firebase.  
- 🖼 **Improved UI**: Add themes, animations, and custom icons.  
- 📈 **Analytics**: Monthly breakdowns, budget limits, and spending alerts.  
- 🌐 **Multi-language Support**.  

---

## 📸 Screenshots (Optional)

_Add app screenshots or GIFs here for better visualization._  

---

## 👨‍💻 Author

**Abinet Bushura Cholo**   
- 🔗 [LinkedIn](https://www.linkedin.com/in/abinet-cholo-a6a13029a)  
- 🐙 [GitHub](https://github.com/Abinet-Cholo)  

---
