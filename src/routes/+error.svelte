<script context="module" lang="ts">
    export function load({ error, status }) {
      return {
        props: {
          status,
          error,
        },
      };
    }
  </script>
  
  <script>
    export let status: number;
    export let error: Error | null;
  </script>
  
  <main>
    <h1>Error {status}</h1>
    {#if error}
      <p>{error.message}</p>
    {:else}
      <p>An unknown error occurred.</p>
    {/if}
    <p>If you see this message means we are doing something. Check back later.</p>
  </main>
  
  <style>
    main {
      padding: 20px;
      background-color: #f8d7da;
      color: #721c24;
      border: 1px solid #f5c6cb;
      border-radius: 5px;
    }
    h1 {
      font-size: 2rem;
    }
  </style>
  