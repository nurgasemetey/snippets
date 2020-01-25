###  one to many relationship spring boot spring data postgre


[Spring Boot, PostgreSQL, JPA, Hibernate RESTful CRUD API Example | CalliCoder](https://www.callicoder.com/spring-boot-jpa-hibernate-postgresql-restful-crud-api-example/ "Spring Boot, PostgreSQL, JPA, Hibernate RESTful CRUD API Example | CalliCoder")


 

```java
package com.example.postgresdemo.model;

import com.fasterxml.jackson.annotation.JsonIgnore;
import javax.persistence.*;
import org.hibernate.annotations.OnDelete;
import org.hibernate.annotations.OnDeleteAction;

@Entity
@Table(name = "answers")
public class Answer extends AuditModel {
    @Id
    @GeneratedValue(generator = "answer_generator")
    @SequenceGenerator(
            name = "answer_generator",
            sequenceName = "answer_sequence",
            initialValue = 1000
    )
    private Long id;

    @Column(columnDefinition = "text")
    private String text;

    @ManyToOne(fetch = FetchType.LAZY, optional = false)
    @JoinColumn(name = "question_id", nullable = false)
    @OnDelete(action = OnDeleteAction.CASCADE)
    @JsonIgnore
    private Question question;

    // Getters and Setters (Omitted for brevity)
}

package com.example.postgresdemo.repository;

import com.example.postgresdemo.model.Answer;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;
import java.util.List;

@Repository
public interface AnswerRepository extends JpaRepository<Answer, Long> {
    List<Answer> findByQuestionId(Long questionId);
}
```
