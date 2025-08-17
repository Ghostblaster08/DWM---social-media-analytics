# DWM---social-media-analytics

This repository contains a social media analytics project designed for deep data mining and analysis of user interactions, platform engagement, and incident tracking such as cyberbullying and scams.

---

## 📊 Star Schema Overview

The database follows a **Star Schema** design, optimized for analytics and reporting. The schema consists of several fact and dimension tables to support efficient querying and aggregation.

### 🟦 Fact Tables

- **Interaction**: Stores data about user interactions with content (posts, likes, comments, etc.).
- **Content_Facts**: Aggregates facts about content posted on platforms.
- **User_Facts**: Aggregates user activity and engagement.
- **Cyber_Bullying/Scams Facts**: Records incidents of cyberbullying or scams.
- **reports**: Tracks individual reports of incidents.

### 🟨 Dimension Tables

- **User**: User information (user_id, user_name, age, gender).
- **Platform**: Platforms where interactions occur (platform_id, name, type).
- **Location**: Geographical location (location_id, country, state, city, pincode).
- **Time**: Date and time breakdown (seconds, year, month, quarter, season).
- **Content**: Content meta-data (content_id, creator, platform, type, etc.).
- **device**: User device details.

---

## 🗺️ Star Schema Diagram

Below is a simplified visual representation of the star schema used in this project:

```plaintext
                  +---------------------+
                  |        User         |
                  +---------------------+
                        ▲
                        |
+---------+       +--------------+         +---------+
| Device  |       | Interaction  |         | Content |
+---------+       +--------------+         +---------+
                        ▲     ▲                ▲
                        |     |                |
                   +----------+----------+     |
                   |          |          |     |
               +-------+  +--------+  +--------+
               |Platform|  |Location|  |  Time  |
               +-------+  +--------+  +--------+

         +---------------------+      +----------------------+
         |    Content_Facts    |      |    User_Facts        |
         +---------------------+      +----------------------+

                    +------------------------------------+
                    |  Cyber Bullying/Scams Facts        |
                    +------------------------------------+
                               ▲
                               |
                         +-----------+
                         |  reports  |
                         +-----------+
```

---

## 📁 Schema Table Details

For column-level details, see the included ER diagrams or refer to the `/schema` directory.

---

## 🚀 Usage

- Load the provided CSVs as mock data to get started.
- Use the schema to build dashboards or advanced analytics.

---

## 📚 References

- See the [ER diagrams](./docs/) for table relationships and column details.

---

*Last updated: 2025-08-17*
