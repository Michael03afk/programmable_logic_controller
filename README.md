# programmable_logic_controller
designed and implemented beginner level parking management system on plc platform
1. Problem Statement
   
In modern urban areas, efficient management of parking spaces is a major challenge. Manual monitoring of parking availability often leads to congestion, time wastage, and inefficient utilization of space. The problem is to design an automated parking system that can monitor vehicle entry and exit, maintain a count of available slots, and control gate operations accordingly.

The system should ensure that vehicles are only allowed entry when parking space is available and prevent overcapacity. A PLC-based control system is used to automate this process using sensors, counters, and logic control.
2. Solution / Methodology
Step 1: Vehicle Detection – Entry and exit sensors detect vehicles.
Step 2: Signal Processing – Signals are sent to PLC.
Step 3: Entry Logic – If space available, open entry gate and increment count.
Step 4: Exit Logic – When vehicle exits, decrement count.
Step 5: Gate Control – Gates operate using timers.
Step 6: Capacity Check – Comparator checks max capacity.
Step 7: Full Condition – If full, entry gate remains closed.
Step 8: Simulation – Implemented using PLC software like Codesys or LogixPro.
Step 9: Monitoring – Display available slots.


4. FLOW CHART
 
<img width="900" height="332" alt="image" src="https://github.com/user-attachments/assets/796c43fd-d59a-4f3d-9774-ae4164e8d36a" />

BLOCK DIAGRAM
The block diagram of the Flow Rate Management System consists of four main sections: input, controller, plant, and feedback. The desired flow rate is given as the reference input to the system. This input is compared with the actual output flow rate, and the error signal is generated. The error signal can be expressed as:
e(t)=r(t)-q(t)….(6)

Where:
r(t)= Desired flow rate
q(t)= Actual flow rate
e(t)= Error signal

The error signal is sent to the MATLAB controller, which generates the control signal u(t)to reduce the error and maintain the required flow rate. The controller output is applied to the flow rate system or plant.
<img width="940" height="139" alt="image" src="https://github.com/user-attachments/assets/dc6d51fb-e147-49c0-83cd-bd0f50bdfd59" />

The plant is represented by the transfer function:
G(s)=(Q(s))/(U(s))=K/(Ts+1)…..(7)

Where:
K= System gain
T= Time constant
The output of the plant is the actual flow rate q(t). This output is continuously measured and fed back to the controller. The feedback signal helps the system compare actual output with desired input and take corrective action automatically.
If the output flow rate is less than the desired value, the controller increases the control signal. If the output flow rate is greater than the desired value, the controller decreases the control signal. Thus, the closed-loop block diagram ensures stable and accurate flow rate control.


