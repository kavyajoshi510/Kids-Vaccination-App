#  Kids Vaccination App

An Android application designed to help parents track the vaccination schedule and birth-related details of their children up to the age of 15 years. With this app, parents can register multiple children, manage birth records, and monitor vaccine progress in a simple and intuitive interface.

---

## 📱 Features

- **User Login & Registration**: Secure authentication for parents.
- **Child Registration**: Register one or more children with complete birth details.
- **Information Page**: View birth-related details of each registered child.
- **Vaccination Progress Page**: Track upcoming and completed vaccines.
- **Multiple Child Support**: A user can manage records for multiple children.

---

## 🧭 Scope of the App

- Assist parents in managing and tracking the vaccination schedule for their kids.
- Provide detailed birth records.
- Display expected vs actual vaccine dates.
- Enable viewing and updating of vaccination progress.
- Facilitate easy registration by parents or close relatives.

---



## 🛠️ Technical Stack

### Software Requirements:
- **Operating System**: Windows 10
- **IDE**: Android Studio
- **Design**: XML
- **Database**: SQLite

### Hardware Requirements:
- **Processor**: Intel i3 or better
- **RAM**: 2 GB or more
- **Storage**: 20 GB or more

---

## 🗂️ Database Design (Data Dictionary)

### `User` Table
| Field | Type | Description |
|-------|------|-------------|
| uid | int (PK) | User ID |
| uname | text (UNIQUE, NOT NULL) | Username |
| password | text (NOT NULL) | Password |

### `Kid` Table
| Field | Type | Description |
|-------|------|-------------|
| id | text (PK) | Kid ID |
| kname | text (UNIQUE, NOT NULL) | Kid’s Name |
| place | text (NOT NULL) | Birthplace |
| date | text (NOT NULL) | Birth Date |
| hospitalname | text (NOT NULL) | Hospital Name |
| bloodgroup | text (NOT NULL) | Blood Group |
| birthweight | real (NOT NULL) | Birth Weight |
| uid | int (FK) | Parent's User ID |

### `Vaccine` Table
| Field | Type | Description |
|-------|------|-------------|
| vid | int (PK) | Vaccine ID |
| vname | text (NOT NULL) | Vaccine Name |
| age | text (NOT NULL) | Recommended Age |
| duedate | text (NOT NULL) | Due Date |

### `kid_vaccine` Table
| Field | Type | Description |
|-------|------|-------------|
| _id | int (FK) | Kid ID |
| vid | int (FK) | Vaccine ID |
| taken_date | text (NOT NULL) | Date Taken |

---

## 🧪 Testing & Validation

### Testing Strategies
- **Unit Testing**: Module-level testing by developers.
- **Integration Testing**: Validation of inter-module connections.
- **System Testing**: Full app integration and behavior testing.

### Sample Test Cases

| Action | Expected Result | Status |
|--------|------------------|--------|
| Valid login | Redirect to home page | ✅ |
| Invalid login | Show error message | ✅ |
| Register new user | User registered | ✅ |
| Duplicate user | Show "User already exists" | ✅ |
| Register new child | Kid registered | ✅ |
| Duplicate kid name | Show "Kid already exists" | ✅ |
| View kids | Show list of registered kids | ✅ |
| View vaccine progress | Show taken vaccines | ✅ |
| Update vaccine progress | Show remaining vaccines | ✅ |

---





## ✅ Conclusion

The **Kids Vaccination App** serves as a helpful and intuitive solution for parents to manage and monitor their child’s health records and vaccination schedule. It simplifies the process of tracking medical milestones and maintains important birth-related data securely.

---

## 📚 Bibliography

### Books:
- *Beginning Android Application Development* – Wei-Meng Lee

### Online References:
- [Android Tutorial – JavaTpoint](https://www.javatpoint.com/android-tutorial)  
- [StudyTonight Android Guide](https://www.studytonight.com/android/)  
- [Android Developer Guide](https://developer.android.com/guide)

---

