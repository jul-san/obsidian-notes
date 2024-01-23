## Software Engineering Ethics
- Involves wider responsibilities than application of technical skills
- Behave in an honest and ethically responsible way to be respected
- Follow a set of principles that are morally correct

## Issues of Professional Responsibility
- Confidentiality
	- Respect confidentiality of a client regardless of a formal agreement

- Competence
	- Should not knowingly accept work outside of their skillset

- Intellectual property rights
	- Be aware of local laws regarding:
		- Patents
		- Copyright
		- etc.
	- Ensure the intellectual property of employers and clients is protected

- Computer misuse
	- Do not use technical skills to misuse others' computers
	- Misuse examples include:
		- Playing games on an employers machine
		- Dissemination of a virus

## Ethical Dilemmas Examples
- Disagreement with policies of senior management
- Releasing safety-critical system without finishing the testing
- Development in military weapons systems or nuclear systems

## Software Diversity (Recap)
- Stand-alone apps
- Interactive transaction-based
- Embedded control systems
- Batch processing systems
- Entertainment systems
- Systems for modeling and simulation
- Data collection systems
- Systems of systems

## Case Studies Overview
| Study                               | Overview                                                                               |
| ----------------------------------- | -------------------------------------------------------------------------------------- |
| Personal Insulin Pump               | Embedded system in an insulin pump used by diabetics to maintain blood glucose control |
| Mentcare: Patient Management System | Used to maintain records of people receiving care for mental health problems           |
| Wilderness Weather Station          | Data collection system that collects data about weather conditions in remote areas     |
| iLearn: Digital Learning Environment                                    | System to support learning in schools                                                                                       |

### Insulin Pump Control System
- Collects data from a blood sugar sensor and calculates the amount of insulin required
- Calculation based on the rate of change of blood sugar levels
- Sends signals to a micro-pump to deliver the correct does of insulin
- Safety-critical system as low blood sugars can lead to:
	- Brain malfunctioning
	- Comas
	- Death
- High-blood sugar levels can lead to:
	- Eye damage
	- Kidney damage

### Insulin Pump Hardware Architecture
![Insulin Architecture][https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.1bX4f1elXwF-YrWWQeD7JgHaEt%26pid%3DApi&f=1&ipt=ce8546fac4a8af5d3870220a89ba6940ec14cdbdee6bacddd2de58c07a146a72&ipo=images]

### Activity Model of Insulin Pump
![Activity Model][https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fedshare.gcu.ac.uk%2F2190%2F2%2FImages%2FImg2.png&f=1&nofb=1&ipt=eda3269e986c26a920ab9d9cfaf4055e2ce3d257d22c79e69256482416742a5a&ipo=images]

### Essential High-Level Requirements
- System must be designed and implemented to meet the requirements:
	- ...

## Mentcare

![Mentcare Architecture][https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fedshare.gcu.ac.uk%2F2190%2F2%2FImages%2FImg3.png&f=1&nofb=1&ipt=c2cec49bea537d6b814e1be490f0b596986fc8a99d159254965aaba35ed0e07f&ipo=images]

- An information system that is intended to use in clinics
- Makes use of a centralized database of patient information
- Designed to run on a laptop
- When the system has a secure network, they use patient info in the database
	- Can be downloaded and use local copies

### Mentcare Goals and Features
- Provide medical staff with timely information to treat patients
	- **Individual Care**: create records for patients
	- **Patient Monitoring**: issue warnings if problems are detected
- Generate management information systems to asses performance against government targets
	- **Administrative Reporting**: calculate statistical information about number of patients, drugs, costs, etc.

### Mentcare System Concerns
- Privacy
	- Essential for patient information to be confidential
	- Cannot be disclosed to anyone other than authorized medical staff and the patient
- Safety
	- Some mental illnesses cause patients to be suicidal or a danger to others
	- System should warn the medical staff about dangerous patients
	- System must be available when need or else prescriptions may be incorrect

### Wilderness Weather Station
- Control over a hundred weather stations in remote areas
- Collect data from a set of instruments that measure:
	- Pressure
	- Sunshine
	- Rainfall
	- Wind speed
	- Wind direction
- Each instrument is controlled by a software system that takes periodic parameter readings
- Manages the data collected from the instruments

### Weather Station's Environment
![Environment][https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F2.bp.blogspot.com%2F-KEkwvHCzTLM%2FUviV_Ca1G7I%2FAAAAAAAAAkI%2FecjYtoENWb8%2Fs1600%2Fweatherstation.png&f=1&nofb=1&ipt=71931ff44e4777f8e76af173979872e1fd670ecb1a8929623ff222e0aa2a5900&ipo=images]

### Weather Information System
- 