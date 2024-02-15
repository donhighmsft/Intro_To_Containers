# ISV & DN COE Todo Application

![Screenshot](https://raw.githubusercontent.com/harunguter/todo-app/main/screenshot.png)

## Run app
```bash
    git clone https://github.com/code-gogo/docker-for-developers-lab-1
    docker-compose up
```

<p>The application is containerized in such a fashion, that the UI is only accessible by accessing `http://localhost` - port 80.</p>
<p>Check the `docker-compose-with-exposed-containers.yml` file for more information on how to expose the container ports.</p>

| Frontend           | API                    |
| :----------------- | :--------------------- |
| `http://localhost` | `http://localhost/api` |

---

## API Reference

#### Get all todos
```http
GET /api/todo
```

#### Get single todo
```http
GET /todo/:id
```
| Parameter | Type     |
| --------- | -------- |
| `id`      | `string` |

#### Add todo
```http
POST /todo
```
```javascript
{
    "content": "string"
}
```

#### Update todo
```http
PUT /todo/:id
```
```javascript
{
    "content": "string"
}
```
| Parameter | Type     |
| --------- | -------- |
| `id`      | `string` |

#### Delete todo
```http
DELETE  /todo/:id
```
| Parameter | Type     |
| --------- | -------- |
| `id`      | `string` |

---
## Tech Stack

**Server:** Nginx
<br>
**Frontend:** React, Semantic UI
<br>
**API:** Node, Express, MongoDB
