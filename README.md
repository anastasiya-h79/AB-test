Учебный проект курса "Симулятор аналитика" от karpov-courses. Состоит из двух блоков: АА-тест и АВ-тест.


АА-тест. Цель - проверка корректности работы системы сплитования. 

Необходимо убедиться, что наша система корректно разбивает пользователей на группы, и ключевая метрика не отличается между группами не только в конкретно нашем АА-тесте, но и в целом. Только если группы до нашего воздействия были "одинаковыми", мы позволим себе утверждать, что возникшее после воздействия отличие вызвано этим воздействием.

У нас есть данные АА-теста с 26 сентября по 2 октября 2022 года. Нужно сделать симуляцию, как будто мы провели 10000 АА-тестов. На каждой итерации сформируем подвыборки без повторения в 500 юзеров из 2 и 3 экспериментальной группы и проведём сравнение этих подвыборок t-критерием Стьюдента.

Нулевая гипотеза H0: μ1​=μ2

Альтернативная гипотеза H1: μ1 <> μ2

Принятый уровень значимости: 5%


AB-test. Цель - проанализировать один из новых алгоритмов рекомендации постов, созданный ML-командой. Цель алгоритма - увеличить вовлеченность пользователей. 

Эксперимент проходил с 2022-11-02 по 2022-11-08 включительно. Для эксперимента были задействованы группы 1 и 2. В группе 2 был использован один из новых алгоритмов рекомендации постов, группа 1 использовалась в качестве контроля.

Нулевая гипотеза заключается в том, что CTR в группах 1 и 2 будут примерно равны. Альтернативная гипотеза заключается в том, что новый алгоритм в группе 2 приведет к увеличению CTR.

План проведения A/B теста:

Сравним CTR в группах 1 и 2, используя следующие методы: t-тест, тест Манна-Уитни, Пуассоновский бутстреп, t-тест на сглаженном ctr (α=5), а также t-тест и тест Манна-Уитни поверх бакетного преобразования.

Сравним результаты каждого метода друг с другом. Посмотрим на распределения нашей величины.

Сделаем выводы на основе полученных результатов.
