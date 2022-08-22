## Design Rest API

### 1. AUTH Services
#### 1.1 Login
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/auth/login </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> None </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"username" : "mashumabduljabbar",
	"password" : "mashum**123"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIwODEyMzQ1Njc4OTAiLCJleHAiOjE2NjA2NzgwNDcsImlhdCI6MTY2MDY2MDA0N30.FINyrqqxXMy4t4Doo7tpxaz9wVU_6hJ4U9yfSIyqFzDJN0yqY_9wNIwnt5JaGiUisU8X5IMlU9qKvJaCoBPfCg"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "timestamp": "2022-08-16T14:28:30.298+0000",
    "status": 401,
    "error": "Unauthorized",
    "message": "Unauthorized",
    "path": "/v1/auth/login"
}
```

</td>
</tr>
</table>
</details>

* * *

### 2. Organization Services
#### 2.1 Create Organization
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/organization </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"organizationCode" : "IKON",
	"organizationName" : "PT Ikonsultan Inovatama",
	"organizationPhone" : "(021)29857220",
	"organizationAddress" : "Beltway Office Park, Jakarta",
	"organizationLat" : "-6.2931353",
	"organizationLong" : "106.8219903",
	"organizationRadius" : 100
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 201,
    "data": {
        "id" : 1,
        "organizationCode" : "IKON",
        "organizationName" : "PT Ikonsultan Inovatama",
        "organizationPhone" : "(021)29857220",
        "organizationAddress" : "Beltway Office Park, Jakarta",
        "organizationLat" : "-6.2931353",
        "organizationLong" : "106.8219903",
        "organizationRadius" : 100,
        "createdAt" : "2022-08-12 17:00:00",
        "updatedAt" : null
	},
    "message": "success"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "timestamp": "2022-08-12T17:00:00.893+07:00",
    "status": 400,
    "error": "Bad Request",
}
```

</td>
</tr>
</table>
</details>

#### 2.2 Read All Data Organization
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/organization </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "ID": 1,
            "organizationCode" : "IKON",
            "organizationName" : "PT Ikonsultan Inovatama",
            "organizationPhone" : "(021)29857220",
            "organizationAddress" : "Beltway Office Park, Jakarta",
            "organizationLat" : "-6.2931353",
            "organizationLong" : "106.8219903",
            "organizationRadius" : 100
            "createdAt": "2022-08-12 07:07:00",
            "updatedAt": null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
</table>
</details>

#### 2.3 Read By Organization Code
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/organization/IKON </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "ID": 1,
            "organizationCode" : "IKON",
            "organizationName" : "PT Ikonsultan Inovatama",
            "organizationPhone" : "(021)29857220",
            "organizationAddress" : "Beltway Office Park, Jakarta",
            "organizationLat" : "-6.2931353",
            "organizationLong" : "106.8219903",
            "organizationRadius" : 100
            "createdAt": "2022-08-12 07:07:00",
            "updatedAt": null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 2.4 Update Organization
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/organization </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> PUT </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"id" : 1,
	"organizationCode" : "IKONS",
	"organizationName" : "PT Ikonsultan Inovatama",
	"organizationPhone" : "(021)29857220",
	"organizationAddress" : "Beltway Office Park, Jakarta",
	"organizationLat" : "-6.2931353",
	"organizationLong" : "106.8219903",
	"organizationRadius" : 100
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "ID": 1,
            "organizationCode" : "IKONS",
            "organizationName" : "PT Ikonsultan Inovatama",
            "organizationPhone" : "(021)29857220",
            "organizationAddress" : "Beltway Office Park, Jakarta",
            "organizationLat" : "-6.2931353",
            "organizationLong" : "106.8219903",
            "organizationRadius" : 100
            "createdAt": "2022-08-12 07:07:00",
            "updatedAt": "2022-08-12 07:08:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 2.5 Delete Organization
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/organization/1 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> DELETE </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "ID": 1,
            "organizationCode" : "IKONS",
            "organizationName" : "PT Ikonsultan Inovatama",
            "organizationPhone" : "(021)29857220",
            "organizationAddress" : "Beltway Office Park, Jakarta",
            "organizationLat" : "-6.2931353",
            "organizationLong" : "106.8219903",
            "organizationRadius" : 100
            "createdAt": "2022-08-12 07:07:00",
            "updatedAt": "2022-08-12 07:08:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

* * *

### 3. Employee Services
#### 3.1 Create Employee
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/employee </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"employeeCode" : "20220800001",
	"employeeName" : "Mashum Abdul Jabbar",
	"employeeGender" : "L",
	"employeePhone" : "0812345678",
	"employeeMail" : "mashum.jabbar@gmail.com",
	"employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
	"employeeAddress" : "Jakarta Timur",
	"organizationCode" : "IKON"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 201,
    "data": {
        "id" : 1,
        "employeeCode" : "20220800001",
        "employeeName" : "Mashum Abdul Jabbar",
        "employeeGender" : "L",
        "employeePhone" : "0812345678",
        "employeeMail" : "mashum.jabbar@gmail.com",
        "employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
        "employeeAddress" : "Jakarta Timur",
        "organizationCode" : "IKON"
        "createdAt" : "2022-08-12 17:00:00",
        "updatedAt" : null
	},
    "message": "success"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "timestamp": "2022-08-12T17:00:00.893+07:00",
    "status": 400,
    "error": "Bad Request",
}
```

</td>
</tr>
</table>
</details>

#### 3.2 Read All Data Employee
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/employee </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : 1,
            "employeeCode" : "20220800001",
            "employeeName" : "Mashum Abdul Jabbar",
            "employeeGender" : "L",
            "employeePhone" : "0812345678",
            "employeeMail" : "mashum.jabbar@gmail.com",
            "employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
            "employeeAddress" : "Jakarta Timur",
            "organizationCode" : "IKON"
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : null
        },
        {
            "id" : 2,
            "employeeCode" : "20220800002",
            "employeeName" : "Dedi",
            "employeeGender" : "L",
            "employeePhone" : "0812345679",
            "employeeMail" : "id.dedi81@gmail.com",
            "employeePhoto" : "1b044a82b59b0ee304dae7416b442b05",
            "employeeAddress" : "Jakarta Barat",
            "organizationCode" : "IKON"
            "createdAt" : "2022-08-12 17:05:00",
            "updatedAt" : null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
</table>
</details>

#### 3.3 Read By Employee Code
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/employee/20220800001 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : 1,
            "employeeCode" : "20220800001",
            "employeeName" : "Mashum Abdul Jabbar",
            "employeeGender" : "L",
            "employeePhone" : "0812345678",
            "employeeMail" : "mashum.jabbar@gmail.com",
            "employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
            "employeeAddress" : "Jakarta Timur",
            "organizationCode" : "IKON"
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 3.4 Update Employee
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/employee </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> PUT </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"id" : 1,
	"employeeCode" : "20220800001",
	"employeeName" : "Mashum Abdul Jabbar",
	"employeeGender" : "L",
	"employeePhone" : "0812345678",
	"employeeMail" : "mashum.jabbar@gmail.com",
	"employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
	"employeeAddress" : "Jakarta Timur",
	"organizationCode" : "IKON"
	"createdAt" : "2022-08-12 17:00:00",
	"updatedAt" : null
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : 1,
            "employeeCode" : "20220800001",
            "employeeName" : "Mashum Abdul Jabbar",
            "employeeGender" : "L",
            "employeePhone" : "0812345678",
            "employeeMail" : "mashum.jabbar@gmail.com",
            "employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
            "employeeAddress" : "Jakarta Timur",
            "organizationCode" : "IKON"
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt": "2022-08-12 07:08:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 3.5 Delete Employee
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/employee/1 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> DELETE </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : 1,
            "employeeCode" : "20220800001",
            "employeeName" : "Mashum Abdul Jabbar",
            "employeeGender" : "L",
            "employeePhone" : "0812345678",
            "employeeMail" : "mashum.jabbar@gmail.com",
            "employeePhoto" : "1b044a82b59b0ee304dae7416b442b04",
            "employeeAddress" : "Jakarta Timur",
            "organizationCode" : "IKON"
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt": "2022-08-12 07:08:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

* * *

### 4. Attendance Services
#### 4.1 Create Attendance
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/attendance </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
	"attendanceLong" : "106.8975194",
	"attendanceLat" : "-6.3402008",
	"attendanceTimezone" : "UTC/GMT +7.00 hours",
	"attendanceType" : "Clock In",
	"employeeCode" : "20220800001"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 201,
    "data": {
        "id" : 1,
        "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
		"attendanceLong" : "106.8975194",
		"attendanceLat" : "-6.3402008",
		"attendanceTimezone" : "UTC/GMT +7.00 hours",
        "attendanceTimeserver" : "2022-08-12 08:00:00",
		"attendanceType" : "Clock In",
		"employeeCode" : "20220800001"
	},
    "message": "success"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "timestamp": "2022-08-12T08:00:00.893+07:00",
    "status": 400,
    "error": "Bad Request",
}
```

</td>
</tr>
</table>
</details>

#### 4.2 Read All Data Attendance
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/attendance </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : 1,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
            "attendanceLong" : "106.8975194",
            "attendanceLat" : "-6.3402008",
            "attendanceLabel" : "WFH",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 08:00:00",
            "attendanceType" : "Clock In",
            "employeeCode" : "20220800001"
        },
		{
            "id" : 2,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b06",
            "attendanceLong" : "106.8975194",
            "attendanceLat" : "-6.3402008",
            "attendanceLabel" : "WFH",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 17:00:00",
            "attendanceType" : "Clock Out",
            "employeeCode" : "20220800001"
        },
        {
            "id" : 3,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b07",
            "attendanceLong" : "106.8219903",
            "attendanceLat" : "-6.2931353",
            "attendanceLabel" : "WFO",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 08:00:00",
            "attendanceType" : "Clock In",
            "employeeCode" : "20220800002"
        },
		{
            "id" : 4,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b08",
            "attendanceLong" : "106.8219903",
            "attendanceLat" : "-6.2931353",
            "attendanceLabel" : "WFO",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 17:00:00",
            "attendanceType" : "Clock Out",
            "employeeCode" : "20220800002"
        }
    ],
	"message": "success"
}

```

</td>
</tr>
</table>
</details>

#### 4.3 Read By Attendance ID
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/attendance/1 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : 1,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
            "attendanceLong" : "106.8975194",
            "attendanceLat" : "-6.3402008",
            "attendanceLabel" : "WFH",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 08:00:00",
            "attendanceType" : "Clock In",
            "employeeCode" : "20220800001"
        }
    ],
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 4.4 Update Attendance
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/attendance </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> PUT </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"id" : 1,
	"attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
	"attendanceLong" : "106.8975194",
	"attendanceLat" : "-6.3402008",
	"attendanceLabel" : "WFH",
	"attendanceTimezone" : "UTC/GMT +7.00 hours",
	"attendanceTimeserver" : "2022-08-12 08:00:00",
	"attendanceType" : "Clock In",
	"employeeCode" : "20220800001"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : 1,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
            "attendanceLong" : "106.8975194",
            "attendanceLat" : "-6.3402008",
            "attendanceLabel" : "WFH",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 08:00:00",
            "attendanceType" : "Clock In",
            "employeeCode" : "20220800001"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 4.5 Delete Attendance
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/attendance/1 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> DELETE </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : 1,
            "attendancePhoto" : "1b044a82b59b0ee304dae7416b442b05",
            "attendanceLong" : "106.8975194",
            "attendanceLat" : "-6.3402008",
            "attendanceLabel" : "WFH",
            "attendanceTimezone" : "UTC/GMT +7.00 hours",
            "attendanceTimeserver" : "2022-08-12 08:00:00",
            "attendanceType" : "Clock In",
            "employeeCode" : "20220800001"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

* * *

### 5. User Services
#### 5.1 Create User
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/user </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"username" : "mashumabduljabbar",
	"password" : "mashum**123",
	"roles" : "USER",
	"status" : "Aktif",
	"employeeCode" : "20220800001"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 201,
    "data": {
        "id" : "1",
        "username" : "mashumabduljabbar",
        "roles" : "USER",
        "status" : "Aktif",
        "employeeCode" : "20220800001",
        "createdAt" : "2022-08-12 17:00:00",
        "updatedAt" : null
	},
    "message": "success"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "timestamp": "2022-08-12T17:00:00.893+07:00",
    "status": 400,
    "error": "Bad Request",
}
```

</td>
</tr>
</table>
</details>

#### 5.2 Read All Data User
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/user </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : "1",
            "username" : "mashumabduljabbar",
            "roles" : "USER",
            "status" : "Aktif",
            "employeeCode" : "20220800001",
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : null
        },
        {
            "id" : "2",
            "username" : "dedi",
            "roles" : "ADMIN",
            "status" : "Aktif",
            "employeeCode" : "20220800002",
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
</table>
</details>

#### 5.3 Read By User Code
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/user/mashumabduljabbar </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": [
        {
            "id" : "1",
            "username" : "mashumabduljabbar",
            "roles" : "USER",
            "status" : "Aktif",
            "employeeCode" : "20220800001",
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : null
        }
    ],
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 5.4 Update User
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/user </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> PUT </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
``` json
{
	"id" : "1",
	"username" : "mashumjabbar",
	"password" : "mashum**123",
	"roles" : "USER",
	"status" : "Aktif",
	"employeeCode" : "20220800001"
}
```

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : "1",
            "username" : "mashumjabbar",
            "roles" : "USER",
            "status" : "Aktif",
            "employeeCode" : "20220800001",
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : "2022-08-12 17:05:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

#### 5.5 Delete User
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL </b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/user/1 </td>
</tr>
<tr>
<td><b> Method </b></td>
<td> DELETE </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": {
            "id" : "1",
            "username" : "mashumabduljabbar",
            "roles" : "USER",
            "status" : "Aktif",
            "employeeCode" : "20220800001",
            "createdAt" : "2022-08-12 17:00:00",
            "updatedAt" : "2022-08-12 17:05:00"
    },
	"message": "success"
}

```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "code": 200,
    "data": null,
    "message": "failed"
}

```

</td>
</tr>
</table>
</details>

* * *

### 6. File Services
#### 6.1 Create File
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> URL</b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/file 

[comment]: <> (https://firebasestorage.googleapis.com/v0/b/<b style="color:orange">ProjectID</b>.appspot.com/o)
[comment]: <> (?uploadType=media&name=<b style="color:orange">filename</b>)

</td>
</tr>
<tr>
<td><b> Method </b></td>
<td> POST </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Params </b></td>
<td> ?uploadType=media&names=<b style="color:orange">filename</b></b></td>
</tr>
<tr>
<td><b> Body </b></td>
<td>
	
<input type="file">

</td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
``` json
{
    "fileName": "filename.png",
    "fileURL": "ProjectID.appspot.com",
    "fileCode": "1660800496188743",
    "createdAt": "2022-08-18T05:28:16.235Z",
    "updatedAt": "2022-08-18T05:28:16.235Z"
}
```

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "error": {
        "code": 400,
        "message": "Invalid HTTP method/URL pair."
    }
}
```

</td>
</tr>
</table>
</details>

#### 6.2 Read File
<details>
<summary> Click to Expand </summary>
<table>
<tr>
<td><b> GET</b></td>
<td> <b style="color:orange">{{baseURL}}</b>/api/v1/file

[comment]: <> (https://firebasestorage.googleapis.com/v0/b/<b style="color:orange">ProjectID</b>.appspot.com/o/<b style="color:orange">filename</b>)
[comment]: <> (?alt=media)

</td>
</tr>
<tr>
<td><b> Method </b></td>
<td> GET </td>
</tr>
<tr>
<td><b> Authorization </b></td>
<td> Bearer Token </td>
</tr>
<tr>
<td><b> Params </b></td>
<td> ?fileCode=1660800496188743</b></td>
</tr>
<tr>
<td><b> Success Response </b></td>
<td>
	
<img src="image\image.png">

</td>
</tr>
<tr>
<td><b> Failed Response </b></td>
<td>
	
``` json
{
    "error": {
        "code": 404,
        "message": "Not Found."
    }
}
```

</td>
</tr>
</table>
</details>