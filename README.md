Download Link: https://assignmentchef.com/product/solved-given-the-er-diagram-and-relation-model
<br>
Given the ER diagram and Relation Model below. Create <strong>four</strong> rows of sample data for each of the relations identified in the <strong>Relational Model</strong>. Based on one of the relations of your relational model and its sample data, specify an <strong>example</strong> of each of the following, and <strong>explain why</strong> you selected it:

A delete operation that would run successfully

An update operation that would run successfully

An update operation that would not run successfully

An insert operation that would not run successfully

<strong><img decoding="async" alt="" data-recalc-dims="1" data-src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F12c%2F12c00506-bc8b-4902-9c48-b0904ce9c77e%2FphpWpHgrU.png?w=980" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/d2vlcm61l7u1fs.cloudfront.net/media%2F12c%2F12c00506-bc8b-4902-9c48-b0904ce9c77e%2FphpWpHgrU.png?w=980" alt="" data-recalc-dims="1">

  </noscript>Deriving Entity types</strong>

Attribute: Primary Key

(fk) : Foreign Key

STUDENT (studentID, firstName, lastName, PhoneNumber, streetNo, streetName, suburb, city, postcode)

STAFF (staffID, firstName, lastName, emailaddress, unitID (fk))

UNIT (staffID, unitName, availableYearSemester)

ASSIGNMENTS (assignmentName, unitName (fk)),dueDateTime)

SLEEPPATTERNS (smartwatchID, totaltimeawake, totaltimeasleep)

<strong>Deriving Relationship types</strong>

STUDENT_STAFF (studentID, tutorID)

Since Student is assigned to Staff a new relation should be created.

STUDENT_UNIT (studentID, unitID)

Since more than one STUDENT is enrolled with more than one UNIT a new relation should be made

STAFF_UNIT (StaffID, unitID)

Since more than one STAFF is assigned to more than one UNIT, a new relation should be created and unitID should be removed from STAFF as it causes redundancy of staff details for every unit if it is assigned to Unit.

STUDENT (studentID, firstName, lastName, PhoneNumber, streetNo, streetName,suburb, city, postcode, smartWatchID(fk))

Since STUDENT has a sleeppatterns, the STUDENT relation should be related tothis by using smartWatchID as a foreign key in STUDENT.

STAFF (staffID, firstName, lastName, emailaddress)

unitID is removed from STAFF.

<strong>Relational Model</strong>

STUDENT (studentID, firstName, lastName, PhoneNumber, streetNo, streetName,suburb, city, postcode, smartWatchID(fk))

STAFF (staffID, firstName, lastName, emailaddress)

UNIT (unitID, unitName, availableYearSemester)

ASSIGNMENTS (assignmentName, unitName (fk)),dueDateTime)

SLEEPPATTERNS (smartwatchID, totaltimeawake, totaltimeasleep)

STUDENT_STAFF (studentID, staffID) both keys are taken from STUDENT AND STAFF relations

STUDENT_UNIT(studentID, unitID) both keys are taken from STUDENT AND UNIT relations

STAFF_UNIT (tutorID, unitID) both keys are taken from STAFF AND UNIT relations

<strong>Constraints</strong>

Postcode in STUDENT SCHEMA should be between 0000 to 9999.

UnitID should be given only between no. of Units in 01 to 99 .

StaffID should be given only between no. of STAFF in 01 to 99 or more and should be assigned only to valid Units with IDs