### fastapi sqlalchemy update 


[python - Update SQLAlchemy ORM existing model from posted Pydantic model in FastAPI? - Stack Overflow](https://stackoverflow.com/questions/63143731/update-sqlalchemy-orm-existing-model-from-posted-pydantic-model-in-fastapi "python - Update SQLAlchemy ORM existing model from posted Pydantic model in FastAPI? - Stack Overflow")


TODO check other ways

```
def update_user(db: Session, user: PydanticUserUpdate):
    """
    Using a new update method seen in FastAPI https://github.com/tiangolo/fastapi/pull/2665
    Simple, does not need each attribute to be updated individually
    Uses python in built functionality... preferred to the pydintic related method
    """

    # get the existing data
    db_user = db.query(User).filter(User.id == user.id).one_or_none()
    if db_user is None:
        return None

    # Update model class variable from requested fields 
    for var, value in vars(user).items():
        setattr(db_user, var, value) if value else None

    db_user.modified = modified_now
    db.add(db_user)
    db.commit()
    db.refresh(db_user)
    return db_user
```
