
# Robotic Arm Torque Calculation 🤖

This project provides torque calculations for a 3-DOF robotic arm, in order to select appropriate servo motors for each joint based on the payload.

## 📐 Arm Specifications
- **Link 1 length:** 10 cm
- **Link 2 length:** 15 cm
- **Gripper length:** 4 cm
- **Payloads tested:** 1 kg and 2 kg
- **Gravity:** 9.81 m/s²

---

## ⚙️ Torque Calculations

### 1. When lifting **1 kg**:
| Joint       | Torque (Nm) |
|-------------|--------------|
| Joint 1     | 2.8449     |
| Joint 2     | 1.8639     |
| Joint 3     | 0.3924     |

### 2. When lifting **2 kg**:
| Joint       | Torque (Nm) |
|-------------|--------------|
| Joint 1     | 5.6898     |
| Joint 2     | 3.7278     |
| Joint 3     | 0.7848     |

---

## 🔍 Motor Selection

### Criteria:
- Torque ≥ calculated value (with 20% safety margin)
- Continuous rotation (for joints) or angular control (for gripper)
- Metal gears preferred

### Suggested Motors:
- **Joint 1:** [Servo Motor MG996R](https://www.amazon.com/MG996R-Digital-Torque-Servo/dp/B00PNEQKC0)
- **Joint 2:** [Servo Motor MG995](https://www.amazon.com/MG995-Servo-Motor/dp/B07CPVHG9H)
- **Joint 3 (Gripper):** [Micro Servo SG90](https://www.amazon.com/TowerPro-SG90-Servo-Motor-Pack/dp/B07CZDTCPD)

---

## ⚠️ Notes & Trade-offs

- **Gears** can be used to multiply torque if needed, but they:
  - Increase complexity
  - Reduce speed
  - Add friction and power loss
- For heavier loads (2 kg), you may:
  - Use **gearing**
  - Choose **higher torque motors**
  - **Shorten the arm** to reduce torque requirements

---

## 🧮 How Torque is Calculated

Torque = Force × Distance  
Where:
- Force = mass × gravity
- Distance = from joint to center of mass of payload

---

## 📎 Author Notes

Prepared for [Smart Methods - الأساليب الذكية] Robotics Program.  
Documented with ❤️ by [Your Name].

