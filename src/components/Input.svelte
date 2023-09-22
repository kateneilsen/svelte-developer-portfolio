<script>
  export let id;
  export let placeholder;
  export let type;
  export let error;
  export let isValid = true;
  export let value = "";

  const onInput = (e) => (value = e.target.value);
</script>

<div class="input">
  <input {type} {id} {placeholder} {value} on:input={onInput} {isValid} />
  {#if !isValid}
    <p class="error">{error}</p>
  {/if}
</div>

<style>
  .input {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }
  .input .error {
    font-size: 12px;
    color: var(--red);
    text-align: right;
  }
  input:invalid {
    border-bottom: 1px solid var(--red);
  }

  input:focus:invalid {
    border-bottom: 1px solid var(--red);
  }

  input {
    border: none;
    border-bottom: 1px solid var(--white);
    background: none;
    color: var(--white);
    padding-block-end: 1rem;
    padding-inline-start: 24px;
    text-transform: uppercase;
  }

  input:focus {
    outline: none;
    border-bottom: 1px solid var(--green);
  }
</style>
