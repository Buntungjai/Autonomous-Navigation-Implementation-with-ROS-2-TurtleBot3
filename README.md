# Autonomous-Navigation-Implementation-with-ROS 2-TurtleBot3

<div align="center">
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/ros2Nav2turtle3.gif" alt="Autonomous Navigation Demo" width="600">
</div>

**วิดีโอสาธิตการใช้งาน:**
- [SLAM & Navigation Overview](https://youtu.be/KPBEK3a9VVg)
- [UPDATE: SLAM & Nav2 with Battery Power](https://youtu.be/AuQmlNzv48g)

โปรเจกต์การพัฒนาหุ่นยนต์ TurtleBot3 Burger ด้วย **ROS 2 Humble** ครอบคลุมตั้งแต่การสร้างแผนที่ (SLAM) ไปจนถึงการนำทางอัตโนมัติ (Autonomous Navigation) ในสภาพแวดล้อมจริง

### 🛠 Hardware & Software Stack
- **Robot:** TurtleBot3 Burger (SBC: Raspberry Pi 4, Controller: OpenCR)
- **Sensor:** 360 Laser Distance Sensor (LDS-01)
- **OS:** Ubuntu 22.04 LTS
- **ROS Version:** ROS 2 Humble Hawksbill
- **Communication:** DDS (Data Distribution Service) ระหว่าง Raspberry Pi 4 และ Remote PC

### 🗺️ SLAM Mapping (Cartographer)
การสร้างแผนที่โดยใช้ Cartographer เพื่อสร้าง Occupancy Grid Map ในพื้นที่ทดสอบ

**การทดสอบช่วงแรก (Power via Adapter):**
ทำการสร้างแผนที่ในขอบเขตจำกัดเนื่องจากข้อจำกัดด้านสายไฟ แต่เห็นผลลัพธ์การขยายพื้นที่ของแผนที่ได้อย่างชัดเจน
<p align="center">
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/before.jpg" width="45%" />
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/after.jpg" width="45%" />
</p>

---

### 🚀 Nav2 & Real-world Implementation
หลังจากติดตั้งระบบแบตเตอรี่ หุ่นยนต์สามารถทำ Nav2 ไปยังตำแหน่งเป้าหมายในพื้นที่จริงได้อย่างอิสระ

<div align="center">
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/nav2.gif" alt="Nav2 Demo" width="600">
</div>

**การทำ SLAM ในพื้นที่ซับซ้อน:**
ทดสอบในห้องที่มีโต๊ะและเก้าอี้จำนวนมาก เพื่อทดสอบความแม่นยำของ Lidar ในการตรวจจับสิ่งกีดขวางขนาดเล็ก
<p align="center">
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/beforeSLAM.jpg" width="45%" />
  <img src="https://raw.githubusercontent.com/Buntungjai/Autonomous-Navigation-Implementation-with-ROS-2-TurtleBot3/main/afterSLAM.jpg" width="45%" />
</p>
