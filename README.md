 🏥 Secure Medical Portal

A web-based **Secure Medical Portal** designed to manage patient information, medical records, appointments, and secure transmission of medical images between authorized healthcare staff.

The platform provides role-based access for healthcare personnel and patients while incorporating secure medical-image handling using image steganography.

📌 Project Overview

The Secure Medical Portal provides a centralized platform for managing healthcare-related information such as:

- Patient profiles and medical information
- Medical records and reports
- Appointments
- Secure medical-image transmission
- Patient history
- Staff authentication
- Role-based access
- Secure communication between healthcare users

The system aims to improve the **security, accessibility, and management of sensitive medical information** within healthcare environments.

✨ Key Features

🔐 Authentication

- Staff login using:
  - Staff ID / Email
  - Hospital ID
  - Password
- Secure password handling using `bcrypt`
- JWT-based authentication
- Session/token-based access control

👨‍⚕️ Patient Management

- View patient information
- Maintain patient records
- Access patient history
- Manage medical information
- Patient-specific dashboards

 📅 Appointment Management

- Appointment scheduling
- View appointment details
- Manage patient-doctor interactions
- Track appointment history

 🩻 Secure Medical Image Transmission

The portal supports secure handling and transmission of medical images using **image steganography**.

Medical images such as:

- X-rays
- MRI scans
- CT scans

can be securely embedded into cover images before transmission.

The system uses a **DSNP – Diagnostic Sensitivity-based Non-sequential Parity Algorithm** to improve the security and preservation of diagnostic information during image embedding.

📁 Medical Records

The platform provides centralized access to:

- Medical reports
- Diagnostic images
- Patient history
- Previous medical records
- Securely transmitted medical images

📊 Dashboards

Separate interfaces are provided for different users to access information according to their roles and permissions.

🏗️ System Architecture

                    ┌─────────────────────┐
                    │      User           │
                    │ Patient / Staff     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Web Interface     │
                    │   HTML / CSS / JS   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Node.js         │
                    │     Express.js      │
                    │     REST APIs       │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┼─────────────┐
                 │             │             │
                 ▼             ▼             ▼
          Authentication   Patient Data   Appointments
                 │             │             │
                 └─────────────┼─────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Secure Image        │
                    │ Processing Module   │
                    │ DSNP Steganography  │
                    └─────────────────────┘
