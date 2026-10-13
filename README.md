# Zadaniya
// 1 задание
function fillArray(length, value) {
    return Array(length).fill(value);
}
console.log(fillArray(5, 2));
// 2 задание
function sortArray(arr) {
    return arr.sort((a, b) => a - b);
}
console.log(sortArray([5, 2, 8, 1, 4]));
// 3 задание
function buildMessage(patient) {
    return "Имя: " + patient.name +
        ", возраст: " + patient.age +
        ", жалобы: " + patient.complaint;
}
console.log(buildMessage({
    name: "Иван",
    age: 20,
    complaint: "Головная боль"
}));
// 4 задание
function hashString(str) {
    let hash = 0;
    for (let i = 0; i < str.length; i++) {
        hash = hash * 31 + str.charCodeAt(i);
    }
    return hash;
}
console.log(hashString("hello"));
// 5 задание
function authorize(success) {
    if (success) {
        return crypto.randomUUID();
    }
    return "Ошибка авторизации";
}
console.log(authorize(true));
// 6 задание
function saveCookie(key, value) {
    document.cookie = key + "=" + value;
}
saveCookie("key", "123");
// 7 задание
function register(login, password) {
    localStorage.setItem("login", login);
    localStorage.setItem("password", password);
}
register("ivan", "12345");
