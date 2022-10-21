  Q: Load Balancer มีความสำคัญอย่างไร ทำไมถึงต้องใช้  จงอธิบายพร้อม ยกตัวอย่าง อย่างละเอียด

  A: Load Balancer หรือการกระจายงานที่เข้ามาไปยัง server หรือ resource ต่าง ๆเพื่อให้ระบบทำงานอย่างมีประสิทธิภารวมทั้งต้องทำให้มั่นใจด้วยว่า ทำการกระจายงานไปยัง server ตามที่ต้องการ
เริ่มด้วยการทำงานแบบ Client-Server โดยถ้ามีผู้ใช้งานมาเพียง 2 คน จะไม่ทำให้เกิดปัญหา แต่เมื่อผู้ใช้งานมีจำนวนมาก ๆ แล้ว แน่นอนก่อให้เกิดปัญหาต่อระบบ เช่นทำงานช้าลง ไม่สามารถรองรับการใช้งานได้
การแก้ไขปัญหามีหลายแนวทาง เช่น
  - การขยายเครื่อง ด้วยการเพิ่ม resource ต่าง ๆ เช่น CPU, Memory และ Network เป็นต้น
  - การเพิ่มเครื่อง server เข้ามาช่วยกันทำงาน

แต่ โดยวิธีการที่ใช้งานบ่อย ๆ คือ การเพิ่มเครื่อง serverเข้ามาช่วยกันทำงาน
  - ทั้งลดปัญหาเรื่อง Single Point of Failure
  - ทั้งลดปัญหาเรื่อง downtime
  - ทั้งช่วยเพิ่มประสิทธฺภาพการทำงานของระบบ
  - ทั้งยังช่วยป้องกันการโจมตีระบบ

จากนั้นจึงต้องมีสิ่งที่เข้ามาช่วยกระจายงานจาก client ไปยัง server ต่าง ๆ อาจจะมองว่าเป็นการแก้ไขปัญหา ด้วยการเพิ่มปัญหามาอีกตัว นั่นก็คือ *** Load Balancer ***
ซึ่งมีหลายเทคนิคให้เลือกใช้งาน ตามความต้องการหรือตามแต่ละ usecase มีดังนี้
  Random selection
  Round Robin
  Weighted Round Robin Method
  Least connection
  Least response time
  Source IP hashing
  
  Ref. https://avinetworks.com/what-is-load-balancing/
