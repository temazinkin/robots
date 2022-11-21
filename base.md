[Назад](README.md)
# Базовый класс робота

Название класса `ФАМИЛИЯ` укажите в&nbsp;точности, как называется файл. Учитывайте заглавные и&nbsp;строчные буквы.

## Методы
Вам предстоит описать реализацию 7 методов класса. Каждый метод отвечает за&nbsp;своё событие. Комментарии подскажут.

### `run()`
Установите внешний вид вашего робота. Задайте цвет корпуса, пушки, радара и&nbsp;пуль. Укажите значение цвета в&nbsp;формате RedGreenBlue. Сделайте своего робота уникальным.

В&nbsp;цикле `while(true)` опишите базовое поведение робота. Что нужно делать, когда вокруг ничего не&nbsp;происходит.

### `onScannedRobot(ScannedRobotEvent enemy)`
Робот понимает, что он&nbsp;не&nbsp;один на&nbsp;поле&nbsp;боя. Поворачивая пушку или радар, вы&nbsp;сможете обнаружить соперников. Когда вражеский робот будет обнаружен, сработает этот метод. Объект `enemy` хранит всю информацию о&nbsp;противнике.

<details>
<summary>Информация о&nbsp;сопернике</summary>
<p><code>enemy.getDistance()</code>&nbsp;— расстояние от&nbsp;вашего центра до&nbsp;центра робота соперника</p>
<p><code>enemy.getVelocity()</code>&nbsp;— скорость противника</p>
<p><code>enemy.getEnergy()</code>&nbsp;— энергия оппонента</p>
</details><br>

### `onHitByBullet(HitByBulletEvent bullet)`
Вас подбили. Срочно примите меры. Опишите, какие действия предпримет ваш робот после попадания в&nbsp;него вражеской пули. Вся информация о&nbsp;выстреле в&nbsp;объекте `bullet`.

<details>
<summary>Информация о&nbsp;пуле</summary>
<p><code>bullet.getBullet()</code>&nbsp;— вся информация о вашей пуле</p>
<p><code>enemy.getHitBullet()</code>&nbsp;— пуля соперника</p>
<p><code>bullet.getBullet().getPower()</code>&nbsp;— мощность вашей пули</p>
<p><code>bullet.getBullet().getVelocity()</code>&nbsp;— скорость вашей пули</p>
<p><code>bullet.getBullet().getX()</code>&nbsp;— координата вашей пули по оси X</p>
<p><code>bullet.getBullet().getY()</code>&nbsp;— координата вашей пули по оси Y</p>
</details><br>

### `onHitWall(HitWallEvent wall)`
Вы&nbsp;столкнулись со&nbsp;стеной. Опишите в&nbsp;этом методе, что нужно делать.

### `onHitRobot(HitRobotEvent enemy)`
Столкновение с&nbsp;другим роботом. Нужно бежать или сражаться. Реализуйте этот метод. Вся информация о&nbsp;сопернике в&nbsp;объекте `enemy`.

<details>
<summary>Информация о&nbsp;сопернике</summary>
<p><code>enemy.getDistance()</code>&nbsp;— расстояние от&nbsp;вашего центра до&nbsp;центра робота соперника</p>
<p><code>enemy.getVelocity()</code>&nbsp;— скорость противника</p>
<p><code>enemy.getEnergy()</code>&nbsp;— энергия оппонента</p>
</details><br>

### `onBulletHit(BulletHitEvent bulllet)`
В&nbsp;яблочко. Вы&nbsp;попали в&nbsp;другого робота. Догнать и&nbsp;добить. Реализуйте алгоритм, что делать после попадания. Объект `bullet` хранит всю информацию о&nbsp;выстреле.

<details>
<summary>Информация о&nbsp;пуле</summary>
<p><code>bullet.getBullet()</code>&nbsp;— вся информация о вашей пуле</p>
<p><code>bullet.getBullet().getPower()</code>&nbsp;— мощность вашей пули</p>
<p><code>bullet.getBullet().getVelocity()</code>&nbsp;— скорость вашей пули</p>
<p><code>bullet.getBullet().getX()</code>&nbsp;— координата вашей пули по оси X</p>
<p><code>bullet.getBullet().getY()</code>&nbsp;— координата вашей пули по оси Y</p>
</details><br>

### `onBulletMissed(BulletMissedEvent bullet)`
Мимо. Опишите в&nbsp;этом методе действия после промаха. Просканируйте обстановку и&nbsp;прицельтесь точнее. Информация о&nbsp;выстреле в&nbsp;объекте `bullet`.

<details>
<summary>Информация о&nbsp;пуле</summary>
<p><code>bullet.getBullet()</code>&nbsp;— вся информация о вашей пуле</p>
<p><code>bullet.getBullet().getPower()</code>&nbsp;— мощность вашей пули</p>
<p><code>bullet.getBullet().getVelocity()</code>&nbsp;— скорость вашей пули</p>
<p><code>bullet.getBullet().getX()</code>&nbsp;— координата вашей пули по оси X</p>
<p><code>bullet.getBullet().getY()</code>&nbsp;— координата вашей пули по оси Y</p>
</details><br>

### Удалите лишнее
Если вы&nbsp;считаете какой-то метод лишним, удалите&nbsp;его.

## Скопируйте код в файл — `фамилия.java`
Замените в&nbsp;коде и&nbsp;в&nbsp;названии файла `фамилия` на&nbsp;свою фамилию. Написать нужно латинскими буквами одинаково в&nbsp;названии файла и&nbsp;в&nbsp;коде.

```java
package practival_work;
import robocode.*;
import java.awt.Color;

public class ФАМИЛИЯ extends Robot
{
	public void run() {
        // внешний вид робота.
        // цвета в формате RGB от 0 до 255
        setBodyColor(new Color(0, 200, 0));
		setGunColor(new Color(0, 150, 50));
		setRadarColor(new Color(0, 100, 100));
		setBulletColor(new Color(255, 255, 100));

        // базовое поведение робота
		while(true) {
            // что делает робот,
            // когда ничего не происходит

		}
	}

	public void onScannedRobot(ScannedRobotEvent enemy) {
        // что делать, когда обнаружен соперник

	}

	public void onHitByBullet(HitByBulletEvent bullet) {
        // что делать, когда вас подбили

	}

    public void onHitWall(HitWallEvent wall) {
        // ваши действия при столкновении со стеной

	}

    public void onHitRobot(HitRobotEvent event) {
        // действия при столкновении с другим роботом

    }

    public void onBulletHit(BulletHitEvent bulllet) {
        // что делать, когда вы попали в другого робота

    }

    public void onBulletMissed(BulletMissedEvent bullet) {
        // что делать, когда вы промахнулись

    }
}
```
