# Production Platform — Docker Swarm, Traefik, CI/CD

**Тип:** эксплуатационные и платформенные задачи · **Компания:** Движком

## Контекст

Несколько backend/frontend сервисов в Docker Swarm, GitLab Runner, реверс-прокси и автоматизированный выпуск изменений.

## Практические задачи

- Построение CI-пайплайнов: линтеры, статический анализ, тестирование, проверки безопасности и сборка образов.
- Разбор GitLab Runner 19 / Docker executor, сетевых тайм-аутов при pull и неверных proxy settings.
- Очистка унаследованных Xray/WireGuard/Amnezia proxy/VPN конфигураций.
- Перенос входного HTTPS-трафика с HAProxy на Traefik.
- Работа с ACME сертификатами, volumes, правами на acme.json и health checks.
- Диагностика режима публикации портов **host vs ingress** и размещения Traefik в Swarm.
- Анализ кворума менеджеров Swarm, размещения реплик и привязки stateful томов.
- Trivy и контроль HIGH/CRITICAL уязвимостей в CI.

## Эффект

По исходному CV, автоматизация снизила время деплоя **с 30 до 10 минут**, а мониторинг и процедуры rollout улучшили устойчивость поставки.

## Инженерные принципы

Воспроизводимость, минимизация ручных действий, наблюдаемость, предсказуемый rollback, отделение stateful и stateless workload, проверка реального маршрута трафика.

## Стек

GitLab CI/CD, GitLab Runner, Docker, Docker Swarm, Traefik, HAProxy, Caddy, Linux, Prometheus/Grafana, Trivy.

[← Проекты](README.md)
