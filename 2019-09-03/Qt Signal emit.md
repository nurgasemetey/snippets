### Qt Signal emit


[Signals &amp; Slots | Qt 4.8](https://doc.qt.io/archives/qt-4.8/signalsandslots.html#a-small-example)




```c++
class Counter : public QObject
{
    Q_OBJECT

public:
    Counter() { m_value = 0; }

    int value() const { return m_value; }

public slots:
    void setValue(int value);

signals:
    void valueChanged(int newValue);

private:
    int m_value;
};
```
