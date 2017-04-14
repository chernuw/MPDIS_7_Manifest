# МПДИС/Мобильные приложения для информационных систем (БГУИР)

 Импорт в Android Studio:
```
File - New... - Project from Version Control - GitHub.
```

Git Repository URL: https://github.com/chernuw/MPDIS_7_Manifest.git

ПРАКТИЧЕСКОЕ ЗАНЯТИЕ  №7. Конфигурирование файла манифеста Android

Цель. Изучить  назначение и возможности конфигурирования манифест файла.


ЗАДАНИЕ.
Создайте графическое изображение размером 48x48 пикселей в любом графическом редакторе.
Добавьте файл с изображением в папку res\drawable-mdpi. Установите атрибут иконки на данный файл и присвойте имени ресурса значение @drawable\myicon. Создайте еще два подобных ресурса но других размеров (36х36 и 72х72). Сохраните их в файлах res\drawable-hdpi, res\drawable-ldpi соответственно.
Выполните регистрацию деятельностей. Для этого создайте новый проект. Выберите узел проекта src и вызовите контекстное меню. Добавьте в этот узел новый класс (деятельности). Присвойте этому классу имя DroidActivity2. Откройте контекстное меню на этом классе и выберите пункт Source. Выберите последовательно опции Override\Implement Methods. Установите флажок рядом с методом onCreate(bundle). Метод будет автоматически добавлен в класс. В теле метода введите setContentView(R.layout.second); Теперь откройте вкладку манифеста и тег Application. В разделе Application Nodes нажмите кнопку ADD. Выберите пункт Activity. В списке просмотра выберите деятельность DroidActivity2. Сохраните изменения и откройте манифест файл. Вы видите, что новая деятельность зарегистрирована, теперь ее можно использовать.
  Задайте требуемую деятельность как основную точку входа в приложение. В манифест-файле установите следующие значения тегов:
  
  ```xml
  <activity
  android:name=".DroidActivity"
  android:label="@string/app_name">
    <intent-filter>
      <action android:name="android.intent.action.MAIN" />
      <category android:name="android.intent.category.LAUNCHER" />      
    </intent-filter>
  </activity>
  ```
 
Далее определите активность запуска. Для этого нужно установить интент-фильтр в теге <intent-filter>:

 ```xml
  <activity
  android:name=".DroidActivity"
  android:label="@string/app_name">
    <intent-filter>
      <action android:name="android.intent.action.MAIN" />
      <category android:name="android.intent.category.LAUNCHER" />      
    </intent-filter>
  </activity>
  ```
 
Создайте варианты приложения с разными точками входа.
Наконец, выполните установку прав доступа. Например, разрешите вашему приложению доступ к камере. Для этого:
Откройте манифест-файл и перейдите на вкладку permissions.Нажмите кнопку ADD и выберите пункт permissions. Введите android.permissions.Camera.
Установите другие права доступа:
-	 к контактам: android.permissions.READ_CONTACTS, android.permissions.WRITE_CONTACTS
-	к WiFi: android.permissions.WIFI_STATE
-	к батарее: android.permissions.BATTERY_STATE
Сохраните файл манифеста.
Программно реализуйте проверку установленных прав доступа.
