RSWEB – Individual Project: MVCHospital (Heights of Health Clinic)
Database structure and relationships
The database consists of four tables: Department, Doctor, Patient, and Appointment.

Relationships between tables:
- Each Doctor is assigned to a Department. This foreign key is not nullable because every doctor working at the hospital must belong to a specific department. The Department–Doctor relationship is one-to-many (1:M).
- Each Patient may be assigned to a Department if they are hospitalized. However, hospitalization is optional, so the foreign key is nullable. The Department–Patient relationship is one-to-many (1:M).
- Appointment is a junction table representing a many-to-many (M:M) relationship between Doctor and Patient. Each Appointment records which Patient was examined and which Doctor performed the examination. One Doctor can examine multiple Patients, and one Patient can have appointments with multiple Doctors.
Implemented functionality
1. Departments
- View all departments, with the option to search and filter by department name.
- Add new departments, edit existing departments, delete departments, and view department details.
- Upload, store, display, modify, and delete an image for each department.
- View doctors assigned to each department.
- By clicking View Doctors, users can see all doctors employed in a particular department, including their information.
- By clicking View Patients for a specific doctor, users can see all patients examined by that doctor, together with their attributes.
- Users can also access the medical report for each patient and view all its details.
The Index page displays a list of departments, including their images and names. Users can filter departments by name, add new departments, edit or delete existing ones, and click on a department's name to view its details and all doctors employed in that department.

The administrator has access to all the views and actions described above.
2. Doctors
- View all doctors, with the option to filter by first name, last name, and specialization.
- Add new doctors, edit existing doctors, delete doctors, and view doctor details.
- Upload, store, display, modify, and delete a profile image for each doctor.
- View patients assigned to each doctor.
- By clicking View Patients, users can see all patients examined by a particular doctor, together with their attributes.
- Users can also access and view the complete medical report for each patient.
The Index page displays a list of doctors, including their profile images, names, and specializations. Users can filter doctors by first name, last name, or specialization, add new doctors, edit or delete existing doctors, and click on a doctor's name to view their details and all patients they have examined.

The administrator has access to all the views and actions described above.
3. Patients
- View all patients, with the option to filter by first name and last name.
- Add new patients, edit existing patients, delete patients, and view patient details.
- View the doctors associated with each patient, including their respective attributes.
- Access the medical report for each appointment a patient has had with a doctor.
- By clicking on a medical report, users can view all its details.
Unlike the Departments and Doctors sections, the Patients Index page displays a list of patients together with all their attributes. Users can filter patients by first name and last name, add new patients, edit existing patient information, delete patients, and view the doctors associated with each patient.

The administrator has access to all the views and actions described above.
4. Appointments
- View all appointments, with the option to filter by the patient's first and last name.
- Add new appointments, edit existing appointments, and delete appointments.
- Upload, store, and play an audio file containing the medical report for each appointment. Existing audio files can also be modified or deleted.
- The Index page displays a list of appointments, including the doctor who performed the examination, the patient who was examined, and the appointment date.
- Users can add new appointments, edit or delete existing appointments, filter appointments by the patient's first and last name, and access the detailed medical report for each appointment.
- By opening a medical report, users can view all appointment attributes, including those not displayed on the Index page.
The administrator has access to all the views and actions described above.

User roles and functionalities
The application supports three different user roles: Administrator, Doctor, and Patient.

Each role has specific permissions and access to different application functionalities.
1. Administrator functionalities
The administrator has full access to the application and can:
- View all doctors, patients, departments, and appointments.
- Add, edit, and delete doctors, patients, and departments.
- View all doctors working in a particular department.
- View all patients assigned to each doctor within a department.
- Access the list of patients through a particular doctor's profile.
- Access the list of doctors associated with a particular patient.
- Add, edit, and delete appointments.
2. Doctor functionalities
Each doctor has access only to their own patients.

Doctors can:
- View a list of their patients, including all relevant patient attributes.
- Access the detailed medical report for each appointment associated with their patients.
- View all attributes included in each medical report.
- Return to their patient list after viewing a medical report.
Editing medical information:

- For outpatients (patients who are not hospitalized), doctors can enter and edit the following information for an appointment:
- Examination
- Diagnosis
- Therapy
- For hospitalized patients, doctors can enter and edit:
- Examination
- Diagnosis
- Therapy
- Appointment date
Doctors can modify the appointment date because these patients are receiving ongoing hospital treatment. Other patient-related fields can be viewed but cannot be modified.

After entering or editing the information, doctors can return to their patient list.

If they decide not to make any changes, they can also return by clicking Back to List of Patients by Doctor.

Any changes made to a medical report are reflected when the doctor opens that report again.

In summary, doctors can:
- View all their assigned patients.
- Edit the permitted medical information for each patient.
- Access the detailed medical report for each appointment.
3. Patient functionalities
Each patient has access only to their own doctors.

Patients can:
- View a list of all doctors who have examined them.
- View the details and attributes of each doctor.
- Access the detailed medical report for each appointment with a particular doctor.
- View all attributes included in the medical report.
- Return to their list of doctors after viewing a report.
Editing medical information:
- For each doctor who has examined them, patients can enter or modify the Symptoms field for a particular appointment.
- All other fields can be viewed but cannot be modified.
After entering or editing the information, patients can return to their list of doctors.

If they decide not to make any changes, they can click Back to List of Doctors by Patient.

Any changes made to the Symptoms field are reflected in the corresponding medical report.

In summary, patients can:
- View all doctors who have examined them.
- Edit the Symptoms field for each appointment.
- Access the detailed medical report for each of their appointments.

Authentication and user account management
The application implements authentication and role-based access control for all three user types: Administrator, Doctor, and Patient.

Each user can log in using an email address and password.

Administrator permissions:
- Register new users.
- Update existing user profiles.
- Delete existing user accounts.
Doctor and Patient permissions:
- Change their own account passwords.
- Access only the functionalities permitted by their respective roles.
All users must be authenticated (logged in) to access the application functionalities described above.
Test login credentials
The following credentials can be used to test the application with different user roles.
Administrator
- Email: admin@mvchospital.com
- Password: Admin123
  
  Doctor
- Email: annetaylor@mvchospital.com
- Password: Anne1234
  
  Patient
- Email: annasmith@mvchospital.com
- Password: Anna1234
