[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/4PO5M1Wx)
# final-project-skeleton

    * Team Name: Beginners
    * Team Members: Kevin Wang, Siyang Li, Fangying Gao
    * Github Repository URL: 
    * Github Pages Website URL: [for final submission]
    * Description of hardware: (embedded hardware, laptop, etc) 

## Final Project Report

Don't forget to make the GitHub pages public website!
If you’ve never made a Github pages website before, you can follow this webpage (though, substitute your final project repository for the Github username one in the quickstart guide):  <https://docs.github.com/en/pages/quickstart>

### 1. Video

[Insert final project video here]

### 2. Images

[Insert final project images here]

### 3. Results

What were your results? Namely, what was the final solution/design to your problem?

#### 3.1 Software Requirements Specification (SRS) Results

Based on your quantified system performance, comment on how you achieved or fell short of your expected software requirements. You should be quantifying this, using measurement tools to collect data.

#### 3.2 Hardware Requirements Specification (HRS) Results

Based on your quantified system performance, comment on how you achieved or fell short of your expected hardware requirements. You should be quantifying this, using measurement tools to collect data.

### 4. Conclusion

Reflect on your project. Some questions to consider: What did you learn from it? What went well? What accomplishments are you proud of? What did you learn/gain from this experience? Did you have to change your approach? What could have been done differently? Did you encounter obstacles that you didn’t anticipate? What could be a next step for this project?

## MVP Demo

What do you plan to accomplish by the MVP Demo?

## Sprint review #2

### Current state of project
### Last week's progress 
### Next week's plan

## Sprint review #1

### Current state of project
### Last week's progress 
### Next week's plan

## Sprint review trial

### Current state of project
### Last week's progress 
### Next week's plan

## Final Project Proposal

### 1. Abstract

For our final project, we will make a smart water bottle with a user interface. The water bottle will be able to monitor the user’s daily water intake, reminding them to drink water on the phone or the website to help them stay hydrated. On top of that, we will include additional features such as water quality testing and a heart rate monitor.


### 2. Motivation

Dehydration poses a real problem in the busy academic and social lives of college students. Many forget to drink enough water throughout the day. This chronic dehydration not only affects physical health but also impacts academic performance, as studies have shown that even mild dehydration can impair cognitive function and concentration.

While there are numerous water bottles available in the market, most serve as simple containers without addressing the root cause of poor hydration habits. Our smart water bottle
project aims to solve this challenge by combining essential hydration tracking with features that appeal to the tech-savvy college demographic. The integration of water quality testing addresses concerns about drinking water safety in various housing situations, while features like the Bluetooth speaker and heart rate monitor transform the bottle into a multi-purpose companion for both studying and exercise, making it more likely to become an essential part of students' daily routines.


### 3. Goals

**11/08**

1. Finalize idea

2. Purchase parts for the smart water bottle

**11/15**

1. Figure out communications between the sensors and MCU

2. Start writing the firmware operating on the smart water bottle

3. Start designing the UI

4. Start configuring wireless communication with the ESP32 module

5. Get a sense of the mechanical dimensions of the water bottle

**11/22**

1. Working out the mechanical parts of the water bottle
   
2. Further develop the firmware by adding additional features such as heart rate monitoring 
   
3. More progress on last week’s items

**11/27**

1. Finish the UI interface
   
2. Finish the firmware 
   
3. Make a working prototype of the mechanical design

**12/4**

1. Finish the final report writing


### 4. System Block Diagram

![alt text](<system bolck diagram.png>)

### 5. Design Sketches

![alt text](<design sketches.png>)

### 6. Software Requirements Specification (SRS)

1. **Overview**

The smart water bottle software system consists of embedded firmware running on the ATmega328PB microcontroller and a companion mobile/web application. The firmware manages sensor data collection, wireless communication, and local user interface, while the companion app provides detailed analytics and user settings management.

2. **Users**

College students (primary users), health-conscious individuals, athletes, fitness enthusiasts, and anyone seeking to improve their hydration habits

3. **Functionality**
   
    1. SRS 01 - Water level shall be measured using capacitive sensing (FDC1004) every 5 seconds with ±5ml accuracy

    2. SRS 02 - TDS measurements shall be performed on demand, with readings completed within 5 seconds
   
    3. SRS 03 - Heart rate shall be measured on-demand when the bottle is held, with readings completed within 15 seconds
   
    4. SRS 04 - The system shall perform wireless communication using the ESP32 Wifi module on the Blynk platform.
   
    5. SRS 05 - The system shall maintain daily water intake records and sync with the mobile app every 15 minutes when connected

    6. SRS 06 - Hydration reminders shall be triggered on the buzzer, displayed on the LCD, and sent through the UI if no water consumption is detected for 2 hours during active hours 
   
    7. SRS 07 - Display shall update every 2 seconds with the current hydration level, water quality, and heart rate measurement when prompted
   
    8. SRS 08 - Buzzer shall sound for five seconds to alert the user if the user stops drinking water for 2 hours.


### 7. Hardware Requirements Specification (HRS)

1. **Overview**
   
The smart water bottle hardware consists of a water-resistant container integrated with multiple sensors, a microcontroller, a display, and wireless communication modules. The system is powered by NiMH batteries and includes a charging circuit.

2. **Functionality**
   
    1. HRS 01 - The project shall be based on an ATmega328PB microcontroller operating at 16M Hz.
   
    2. HRS 02 - FDC1004 capacitive sensing system shall be implemented with:
        - 4 vertical sensing electrodes on PCB
  
        - Ground shield for noise reduction

        - Waterproof conformal coating

        - Detection range of 0-750ml

        - Resolution of ±5ml

    3. HRS 03 - LCD shall output heart rate and water consumption when prompted
   
    4. HRS 04 - The system shall use the ESP32 module 
  
    5. HRS 05 - MAX30102 heart rate sensor shall be integrated with an accuracy of ±3 BPM
   
    6. HRS 06 - TDS sensor shall measure water quality in a range of 0-1000ppm with ±2% accuracy

    7. HRS 07 - System shall be powered by 4x AA NiMH batteries (2000mAh each) with:

        - Total voltage: 4.8V

        - MAX712 charging IC

        - Reverse polarity protection

        - Low battery detection

    8. HRS 08 - TDS PCB shall be:
   
        - Sealed with conformal coating

        - Include temperature compensation electrode

        - Appropriately sized for portability

    9. HRS 09 - Capacitive sensing PCB shall be:

        - Integrated between bottle layers

        - Sealed with conformal coating

        - Maintain sensitivity through bottle wall (≤3mm thickness)

    10. HRS 10 - System enclosure shall be:

        - Provide easy access to battery replacement

        - Maintain a water-tight seal around the sensor strip

    11. HRS 11 - Power Management shall be:

        - Main power rail: 4.8V from NiMH batteries

        - Reverse polarity protection

        - Overcurrent protection (2A fuse)

        - Short circuit protection

        - Linear voltage regulator shall maintain the appropriate working voltage for each component


### 8. Components

1. **Input Devices**
   
    1. FDC1004

        - Type: Water Level Sensor (I2C)
  
        - Quantity: 1

        - Price: $1.20
  
        - Voltage Range: 3 - 3.6V
  
        - Link: FDC1004 Datasheet
  
        - Function: Non-contact water level sensing based on capacitance changes
   
    2. SEN0244
   
        - Type: Water Quality Sensor Dev Board
 
        - Quantity: 1
  
        - Price: $11.85

        - Voltage Range: 3.3 - 5.5V
  
        - Link: SEN0244 Datasheet
  
        - Function: Measures parameters like pH or turbidity. May require a custom PCB due to size
  
    3. MAX30102
   
        - Type: Heart Rate Monitor (I2C)
  
        - Quantity: 1
  
        - Price: $14.19
  
        - Voltage Range: 1.7 - 2.0V
  
        - Link: MAX30102 Datasheet
  
        - Function: Measures heart rate and oxygen saturation via photoplethysmography (PPG)
  
    4. ESP32
   
        - Type: WiFi Module
  
        - Quantity: 1
  
        - Price: $0.00 (already owned)
  
        - Voltage Range: 2.3 - 3.6V
  
        - Function: Provides WiFi connectivity

2. **Power System**
   
   1. 4x Panasonic Eneloop AA NiMH Batteries
  
        - Type: NiMH Batteries
  
        - Quantity: 4
  
        - Price: $14.90
  
        - Link: Eneloop Batteries
  
        - Function: Rechargeable batteries for the main power supply
  
   2. LM1117
  
      - Type: Voltage Regulator
  
      - Quantity: 1
  
      - Price: $0.61
  
      - Voltage Range: 2.6 - 15V
  
      - Link: LM1117 Datasheet
  
      - Function: Regulates the battery voltage to a stable 3.3V output
  
   3. MAX712
  
      - Type: Charging IC
  
      - Quantity: 1
  
      - Price: $3.95
  
      - Voltage Range: 4.5 - 5.5V
  
      - Link: MAX712 Datasheet
  
      - Function: Manages NiMH battery charging

3. **Output Devices**

   1. Buzzer
  
      - Type: Audio Output
 
      - Quantity: 1
  
      - Price: $0.00 (already owned)
  
      - Voltage Range: 3.3V - 5V
  
      - Function: Provides audio alerts
  
   2. LCD Display
  
      - Type: Display

      - Quantity: 1
  
      - Price: $0.00 (already owned)
  
      - Voltage Range: 5V
  
      - Function: Displays real-time data and user interface information


### 9. Final Demo

We aim to have a smart water bottle with all the required functionality and a working user interface in the final demo. Meanwhile, we’ll optimize the size and portability of the water bottle as much as possible during our allocated time for the final project.


### 10. Methodology

Our approach to developing the smart water bottle will follow the three phases below:

**Phase 1**: 

  - Design and implement the basic water bottle structure with water-proof housing
  
  - Develop a reliable water level tracking system using capacitative sensors
  
  - Implement the Wifi module with the water bottle

**Phase 2**: 

  - Add water quality (TDS) monitoring system
  
  - Integrate heart rate sensor 
  
  - Develop an intelligent reminder system based on user patterns
  
  - Create a user interface

**Phase 3: Testing and Optimization**

  - Conduct water-resistance testing under various conditions
  
  - Test sensor accuracy and calibration
  
  - Validate data synchronization reliability
  
  - Optimize the size and portability of the water bottle.


### 11. Evaluation

We will evaluate our smart water bottle's success using multiple quantitative and qualitative metrics:

**Sensor Accuracy**

  - Water Level: ±5ml accuracy in measurements
   
  - TDS: ±2% deviation from laboratory water quality measurements
   
  - Heart Rate: ±3 BPM compared to medical-grade monitor

**Reliability**

  -  All sensors are functional with specified accuracy
   
  - Reliable water level tracking
   
  - Punctuality of reminders during active time
    
  - Water-resistant operation


### 12. Proposal Presentation

Add your slides to the Final Project Proposal slide deck in the Google Drive.

## References

Fill in your references here as you work on your proposal and final submission. Describe any libraries used here.

## Github Repo Submission Resources

You can remove this section if you don't need these references.

* [ESE5160 Example Repo Submission](https://github.com/ese5160/example-repository-submission)
* [Markdown Guide: Basic Syntax](https://www.markdownguide.org/basic-syntax/)
* [Adobe free video to gif converter](https://www.adobe.com/express/feature/video/convert/video-to-gif)
* [Curated list of example READMEs](https://github.com/matiassingers/awesome-readme)
* [VS Code](https://code.visualstudio.com/) is heavily recommended to develop code and handle Git commits
  * Code formatting and extension recommendation files come with this repository.
  * Ctrl+Shift+V will render the README.md (maybe not the images though)
