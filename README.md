## 0. Preconditions for code to run

> #### **How ​​does the system run? </u>**

> 1. Configure the mongoDB database environment (you can install mongodb compass locally, the local database will be installed by default, localhost:27017 will connect to the database, create vue_webgis/users, and the registered user can log in after running the program), or you can choose the online mongodb database, modify You can configure the database connection in config.
> 2. cd client
> 3. npm install (install dependencies in client code)
> 4. cd ../
> 5. npm install (install dependencies in the server code)
> 6. npm run dev (front-end and back-end serialization, start front-end and back-end at the same time)

## 1. Effect display
**System login**
![loginPage.png](https://i.loli.net/2021/11/17/reFpu5ABTdi8zoX.png)

---

**Map home page, support the switching of multi-source online network maps such as Google, Tiantu, AutoNavi, Tencent, Geoq, ArcGIS, etc.**
> Google Maps public imagery removed (January 2021)
> Adjust the confusion of the original code view and components; MapBox map component encapsulation, data layer loading component, map basemap switching component; (2021.1.31)

![mapHomePage.png](https://i.loli.net/2021/11/17/fSaKQCoZXeH3uzJ.png)

---

**3D building map, loading GeoServer 3D building vector tiles based on MapBoxGL**
![3Dbuilding.png](https://i.loli.net/2021/11/17/NYyTzPI2LD4cURE.png)

---

**MapBox custom basemap**
![mapbox01.png](https://i.loli.net/2021/11/17/3eMyHIYaRXp6FfV.png)

---
**MapBoxgl drawing**
![mapbox_draw.png](https://i.loli.net/2021/11/17/6JMmO9l2QHEuvVN.png)

---
**MapBoxGL integrates deck.gl for high-performance visualization**
![HexgonMap.png](https://i.loli.net/2021/11/17/8qBGaTFMpy6Z7HX.png)

---

**openlayers aggregate graph**
![openlayerCluster.png](https://i.loli.net/2021/11/17/lR9tv6hEbdAXDJK.png)

---
**openlayers crop map basemap**
![openlayerClip.png](https://i.loli.net/2021/11/17/ilWN9UVp7hSewat.png)

---

<!--There are many interesting functions in the system waiting for you to discover-->
**arcgis api 4.x**
![arcgisHomePage.png](https://i.loli.net/2021/11/17/OCAEdesBVj4Rg7v.png)

<!--The follow-up map function is gradually improving, and will try to use a variety of map apis and integrate gis related libraries-->

## 2. VUE + Node + WebGIS project description:

### 2.1 Practical purpose: use modular programming based on the VUE framework to realize the development of WebGIS

### 2.2 Main Features
1. Front-end and back-end project construction
2. Login and register (token verification function)
3. Rich map development api DEMO integration, map visualization implementation

### 2.3 Main Technology

> Map Framework: MapBoxGL/openlayers 5.x / ArcGIS API 4.x

> Build interface documentation: Node + express + jwt;

> Build front-end pages: VueCli 3.0 + ElementUI

> Data request and interception: Axios + MongoDB

> Other upcoming or already used technologies: GeoServer, PostGIS, deck.gl, echarts,

### 2.4 Project construction details

#### (1) Preparations
1.1 Build a server (based on express)

1.2 Connect to the local MongoDB database

1.3 Build routing and data model

#### (2) Login registration interface
express's body-parser middleware

> bcrypt encryption module

> jsonwebtoken

Get token (to get data token/jsonwebtoken)-----verify token (passport/passport-jwt)


#### (3) Passport verification



#### (4) Front-end and back-end serialization 
