# GEIAL322-BL2
Adatbázisrendszerek I.


```mermaid
erDiagram
    STUDENT {
        int StudentID
        string Name
        int Age
        int ClassID
    }
    TEACHER {
        int TeacherID
        string Name
        string Specialization
    }
    CLASS {
        int ClassID
        string ClassName
        int HeadTeacherID
    }
    SUBJECT {
        int SubjectID
        string SubjectName
        int Credit
    }

    STUDENT ||--o| CLASS : "belongs to"
    STUDENT }o--|| SUBJECT : "takes"
    TEACHER }o--|| SUBJECT : "teaches"
    TEACHER }o--|| CLASS : "teaches"
    CLASS ||--o{ SUBJECT : "includes"

```
