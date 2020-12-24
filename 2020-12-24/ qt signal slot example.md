###  qt signal slot example


[Signals &amp; Slots | Qt 4.8](https://doc.qt.io/archives/qt-4.8/signalsandslots.html "Signals &amp; Slots | Qt 4.8")


 

```
#include <QObject>

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



void Counter::setValue(int value)
{
    if (value != m_value) {
        m_value = value;
        emit valueChanged(value);
    }
}


    Counter a, b;
    QObject::connect(&a, SIGNAL(valueChanged(int)),
                     &b, SLOT(setValue(int)));

    a.setValue(12);     // a.value() == 12, b.value() == 12
    b.setValue(48);     // a.value() == 12, b.value() == 48


Calling a.setValue(12) makes a emit a valueChanged(12) signal, which b will receive in its setValue() slot, i.e. b.setValue(12) is called. Then b emits the same valueChanged() signal, but since no slot has been connected to b's valueChanged() signal, the signal is ignored.



```
