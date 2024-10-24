<script>
    const cards = [
        { date: '15 августа', name: 'Расписание занятий' },
        { date: '12 августа', name: 'Прикрепленные файлы' },
        { date: '11 августа', name: 'Лабораторная работа #5' },
        { date: '9 августа', name: 'Студенческая весна. Фото и...' },
        { date: '5 августа', name: 'Список на отчисление' },
        { date: '4 августа', name: 'Прикрепленные файлы' },
        { date: '2 августа', name: 'Расписание занятий' },
        { date: '1 августа', name: 'Студенческая весна. Фото и...' },
        { date: '26 июля', name: 'Лабораторная работа #5' },
        { date: '22 июля', name: 'Расписание занятий' },
        { date: '21 июля', name: 'Лабораторная работа #5' },
        { date: '16 июля', name: 'Прикрепленные файлы' },
        { date: '12 июля', name: 'Студенческая весна. Фото и...' },
        { date: '6 июля', name: 'Список на отчисление' },
        { date: '5 июля', name: 'Расписание занятий' }
    ];
</script>

<div class="main-section">
    <div class="interactions">
        <h1>Учебные материалы</h1>
        <div id="add-button">
            <img src="/+.png" alt="Добавить" />
            <p>Добавить пост</p>
        </div>
    </div>
    <div class="files-card-view">
        {#each cards as card}
            <div class="card">
                <div class="date">Добавлено {card.date}</div>
                <div class="name">{card.name}</div>
                <div class="open-button">Подробнее</div>
            </div>
        {/each}
    </div>
    <div class="more-button">
        <img src="/arrow.png" alt="Показать еще" />
        <p>Показать еще</p>
    </div>
</div>

<style>
    .main-section {
        max-width: 100%;
    }
    .interactions {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 1rem;
    }
    #add-button {
        color: white;
        padding: 0.5rem 1rem;
        border-radius: 10px;
        background-color: rgba(166, 200, 30, 1);
        display: flex;
        align-items: center;
        gap: 0.5rem;
        cursor: pointer;
    }
    .files-card-view {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
    }
    .card {
        background-color: rgba(0, 0, 0, 0.03);
        flex: 1 1 calc(20% - 1rem); /* Adjusted to fit 5 cards in one row */
        padding: 1rem;
        border-radius: 10px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        aspect-ratio: 1 / 1; /* Makes the card a square */
        margin-bottom: 1rem; /* Added margin-bottom to create distance between rows */
    }
    .card .date {
        color: rgba(131, 131, 131, 1);
        font-size: 0.875rem;
        margin-bottom: 0.5rem;
    }
    .card .name {
        font-size: 1.25rem;
        margin-bottom: 1rem;
        word-wrap: break-word;
    }
    .card .open-button {
        border: 2px solid rgba(166, 200, 30, 1);
        color: rgba(166, 200, 30, 1);
        border-radius: 10px;
        font-size: 0.875rem;
        padding: 0.5rem;
        text-align: center;
        cursor: pointer;
    }
    .more-button {
        border: 2px solid rgba(166, 200, 30, 1);
        border-radius: 10px;
        color: rgba(166, 200, 30, 1);
        padding: 0.5rem;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
        cursor: pointer;
        margin-top: 1rem;
    }

    @media (max-width: 1920px) {
        .card {
            flex: 1 1 calc(15% - 1rem); /* Adjusted to fit 5 cards in one row */
        }
    }

    @media (max-width: 768px) {
        .card {
            flex: 1 1 calc(33.33% - 1rem); /* Adjusted to fit 3 cards in one row */
        }
    }

    @media (max-width: 480px) {
        #add-button p{
            display: none;
        }
        .card {
            width: calc(50% - 1rem); /* Adjusted to fit 1 card in one row */
        }
    }
</style>
