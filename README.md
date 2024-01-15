# BnB Plateform

## Entities

### Review
This entity represents a review made by a traveler to a booking from a room.

| Property   | Type      | Description                | Relationship |
| ---------- | --------  | -------------------------- | ------------ |
| title      | string    | 50 NOT NULL                |              |
| comment    | text      | NOT NULL                   |              |
| rating     | integer   | NOT NULL                   |              |
| created_at | datetime  | NOT NULL                   |              |
| traveler   | ManyToOne | NOT NULL, OrphelanTrue     | User         |
| rooms      | ManyToOne | NOT NULL, OrphelanTrue     | Room         |

### Booking

| Property    | Type      | Description             | Relationship |
| ----------- | --------  | ------------------------| ------------ |
| number      | string    | 50 NOT NULL             |              |
| chek_in     | datetime  | NOT NULL                |              |
| chek_out    | datetime  | NOT NULL                |              |
| occupants   | ingteger  | NOT NULL                |              |
| created_at  | datetime  | NOT NULL                |              |
| traveler    | ManyToOne | NOT NULL, OrphelanTrue  |User          |
| room        | ManyToOne | NULL, OrphelanTrue      |Room          |
| review      | OneToOne  | NULL, OrphelanTrue      |Review        |

### Equipement
This entity 

| Property  | Type      | Description   | Relationship |
| ----------| --------- | --------------| ------------ |
| name      | string    | 50 NOT NULL   |              |
| rooms     | ManyToOne | NOT NULL      | Room         |