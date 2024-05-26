<script setup lang="ts">

</script>

<template>
  <Card class="w-[350px] p-4">
    <CardHeader>
      <CardTitle>Добавить аниме</CardTitle>
      <CardDescription>Форма добавления аниме на сайт</CardDescription>
    </CardHeader>
    <CardContent>
      <form>
        <div class="grid items-center w-full gap-4">
          <div class="flex flex-col space-y-1.5">
            <Label for="animeName">Название</Label>
            <Input id="animeName" placeholder="Введите название аниме" />
          </div>
          <div class="flex flex-col space-y-1.5">
            <Label for="genre">Жанр</Label>
            <Select>
              <SelectTrigger id="genre">
                <SelectValue placeholder="Выбрать" />
              </SelectTrigger>
              <SelectContent position="popper">
                <SelectItem value="hentai">
                  Хентай
                </SelectItem>
                <SelectItem value="Ya-oi">
                  Яой
                </SelectItem>
                <SelectItem value="Yuri">
                  Юри
                </SelectItem>
                <SelectItem value="hard">
                  Жоское
                </SelectItem>
              </SelectContent>
            </Select>
          </div>
        </div>
      </form>
    </CardContent>
    <CardFooter class="flex justify-between px-6 pb-6">
      <Button variant="outline">
        Отмена
      </Button>
      <Button>Опубликовать</Button>
    </CardFooter>
  </Card>
</template>

<style scoped>

</style>