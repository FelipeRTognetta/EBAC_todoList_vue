<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    class="form-control" type="text" placeholder="Digite aqui a descrição da tarefa">
            </div>

            <div class="col-md-2">
                <button class="btn btn-primary" type="submit">Cadastrar</button>
            </div>

            <div class="col-md-2">
                <select class="form-control" @change="props.trocarFiltro">
                    <option value="todas">Todas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>