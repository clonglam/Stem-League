
![cover](https://user-images.githubusercontent.com/86845927/165398689-4ab8e27d-5197-483a-8eca-bf85dd106087.png)

Hi guys, This is a Project called STEM-League, which is a learning tool kit for steam learning started by me and two of my friends. I created the software parts of the project including low latency control via the web dashboard and software control on Rpi. It is currently used in a secondary school for learning STEM. 

# STEM-League
Stem League is a web controling dashboard, We would like to design a system that control the stem larnging tool kits installed in the room, and I use react, socketio and rpi created a system that secure, safe and low latency.

This system included two parts, one web controling system and stem learning hardware component. I responsibe to design and create the system, This system is currently using in a Hong Kong Secondry school.

| Problem                                                                                                                                                                                                                                                                                                                           | Solution                                                                                                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The system need to be Saftey, Secure and Low-latency. It is installed in school, saftey is a must, we need to ensure only authorized teacher can use it. Secure, We need to ensure the user can only control in the installed room. Low-latency, if there is high latency, it is bad in control, and it may cause saftey problem. | We use Socket.io to create a low-latency control environment, and required the use login-in before that get into the control board. They need to pass through auth middleware, before the command really send to hardware |

## Low-Latency

To provide a good controling response, low-latency is needed. We designed to use Socket.io to pass the data. When the user move the control stick in the dashboard, the front in will pass the data to the component via WebSockets. and it created nearly instant response. Advanced by the socket.io, it provide a low-latency and safety environment for user.

![StemRing_Lowlatency](https://www.clong.pro/assets/blog/stem-league/move_Left.gif)

## Secuity

We need to encsure the user is authorized users. Users are required login before using the system. Before sending the data to the hardware, data are need to pass the auth middleware first. We can ensure only auorized users can control those hardware but not anyone.

![webDashboard]([https://user-images.githubusercontent.com/86845927/183285445-93707b2d-1de7-4f67-8c3f-8a72448597ad.png](https://www.clong.pro/assets/blog/stem-league/stemring_anim.gif))
