<footer class="footer">
    <p>&copy; 2025 Portfolio. All rights reserved.</p>
</footer>


<style>
    .footer {
        width: 100%;
        padding: var(--space-md);
        text-align: center;
        font-family: var(--font-body);
        font-size: var(--font-sm);
        background-color: var(--background-tertiary);
        position: relative;
        z-index: 10;
    }

    .footer::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        height: 15px;
        width: 100%;
        background: var(--divider-color);
    }

    .footer p {
        color: var(--text-secondary);
    }

    @media (max-width: 768px) {
        .footer {
            padding: var(--space-sm);
            font-size: var(--font-xs);
        }
    }
</style>
