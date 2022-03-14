1. На локальном репозитории сделать ветки для:
    - Postman  
        `git branch Postman`  
    - Jmeter  
        `git branch Jmeter`  
    - CheckLists  
        `git branch Checklist`  
    - Bag Reports  
        `git branch Bug_Reports`  
    - SQL  
        `git branch SQL`  
    - Charles  
        `git branch Charles`  
    - Mobile testing  
        `git branch Mobile_Testing`  
2. Запушить все ветки на внешний репозиторий  
    - `git push -u origin Postman`  
    - `git push -u origin Jmeter`  
    - `git push -u origin Checklists`  
    - `git push -u origin Bug_Reports`  
    - `git push -u origin SQL`  
    - `git push -u origin Charles`  
    - `git push -u origin Mobile_Testing`
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта  
    `git checkout Bug_Reports`  
    `touch bug_report.md`  
    `vim bug_report.md`  
    `i`  
    ```
    № | name | description
    ---- |---- | -----
    **1** | *ID* | Уникальный идентификационный номер
    **2** | *Summary/Title* | Что? Где? При каких обстоятельствах/условиях?
    **3** | *STR* | Шаги воспроизведения
    **4** | *Actual Result* | Фактический результат
    **5** | *Expected Result* | Ожидаемый результат
    **6** |*Environment* | Окружение (н. Dev/Stage/Prod)
    **7** | *Project* | Название проекта
    **8** | *Module* | Компонент/модуль/юнит, в котором обнаружен дефект
    **9** | *Build* | Версия сборки
    **10** | *Severity* | Критичность бага по степени влияния на продукт
    **11** | *Priority* | Критичность бага по степени влияния на бизнес
    **12** | *Status* | Статус бага в жизненном цикле бага
    **13** | *Author* | Тот, кто нашёл баг
    **14** | *Assigned to* | Назначение
    **15** | *Attachments* | Логи/скриншоты/видео
    ```  
    ESC `:wq` ENTER  

4. Запушить структуру багрепорта на внешний репозиторий  
    `git add bug_report.md`  
    `git commit -m "Add new file bug_report.md"`  
    `git push`  
5. Вмержить ветку Bag Reports в Main  
    `git checkout main`  
    `git merge Bug_Report`  
6. Запушить main на внешний репозиторий.  
    `git push`  
7. В ветке CheckLists набросать структуру чек листа.  
    `git checkout Checklists`  
    `touch checklist.md`  
    `vim checklist.md`  
    `i`  
    ```
    ## Кто, где и когда будет тестировать
    | name  |  description |    
    | ---- | ---- |
    | *build* |   версия сборки |
    | *environment* |   окружение |
    | *test date* |   дата проведения теста |
    | *tester* | тестировщик |

    ## Stand alone module checks
    name | description
    ---- | ----
    Test type | Тип/вид/уровень тестирования
    Checking | Название проверки
    Result | Результат  
    ```  
    ESC `:wq` ENTER  

8. Запушить структуру на внешний репозиторий  
    `git add checklist.md`  
    `git commit -m "Add new file checklist.md"`  
    `git push`  
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main  
    Зайти на сайт [github](https://github.com/)  
    
    Выбрать репозиторий [group_27](https://github.com/bryack/group_27)  
    
    Нажать на кнопку `Compare & pull request`  
    ![Compare & pull request](https://github.com/bryack/group_27/blob/Checklists/Compare_pull_request.png?raw=true)    
    
    Под заголовком Open a pull request должно быть указано `Able to merge`  
    ![Able to merge](https://github.com/bryack/group_27/blob/main/Able_to%20merge.png?raw=true)  
    
    В текстовом поле заголовка написать *Add new file checklist.md from Checklists branch*  
    
    Нажать на кнопку `Create pull request`  
    ![Create pull request](https://github.com/bryack/group_27/blob/main/Create_pull_request.png?raw=true)  
    
    После проверки возможности слияния веток должно быть указано `This branch has no conflicts with the base branch`  
    ![No branches conflicts](https://github.com/bryack/group_27/blob/main/No_branches_conflicts.png?raw=true)  
    
    Нажать на кнопку `Merge pull request`  
    ![Merge pull request](https://github.com/bryack/group_27/blob/main/Merge_pull_request.png?raw=true)  
    
    Нажать на кнопку `Confirm merge`  
    ![Confirm merge](https://github.com/bryack/group_27/blob/main/Confirm_merge.png?raw=true)  
    
    После слияния веток должно быть указано `Pull request successfull merged and closed`  
    ![Pull request success](https://github.com/bryack/group_27/blob/main/pull_requst_success.png?raw=true)  

10. Синхронизировать Внешнюю и Локальную ветки Main  
    `git checkout main`  
    `git pull`  