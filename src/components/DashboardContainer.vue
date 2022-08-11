<script lang="ts" setup>
import NavMenu from "./NavMenu.vue";
import SearchBox from "./SearchBox.vue";
import ChooseField from "./ChooseField.vue";
import FileList from "./FileList.vue";
import FileListItem from "./FileListItem.vue";
</script>

<template>
  <div class="dashboardContent">
    <nav-menu>
      <div class="Logo">Document<span>Office</span></div>
      <SearchBox
        srcImageSearch="@/assets/search-icon-32x32.svg"
        srcImageCancelSearch="@/assets/cancel-icon-32x32.svg"
      />
      <div class="Buttons"></div>
    </nav-menu>

    <div class="templatesDocs">
      <div class="templatesDocs_tD">
        <span>utwórz nowy dokument</span>
        <button>Galeria szablonów</button>
        <div class="separator"></div>
        <button class="optionButton">
          <img src="@/assets/option-icon.svg" alt="option_icon" />
        </button>
      </div>
      <div class="templateList">
        <div class="templateItem">
          <div class="templateIcon"></div>
          <div class="templateLabel">Pusty</div>
        </div>
        <div class="templateItem">
          <div class="templateIcon"></div>
          <div class="templateLabel">Życiorys</div>
          <span>Szeryfowy</span>
        </div>
        <div class="templateItem">
          <div class="templateIcon"></div>
          <div class="templateLabel">Życiorys - koralowiec</div>
          <span>Koralowiec</span>
        </div>
        <div class="templateItem">
          <div class="templateIcon"></div>
          <div class="templateLabel">Mięta</div>
          <span>Mięta</span>
        </div>
        <div class="templateItem">
          <div class="templateIcon"></div>
          <p class="templateLabel">Propozycja projektu</p>
          <span>Tropiki</span>
        </div>
      </div>
    </div>
    <div class="lastDocs">
      <span>Ostatnie dokumenty</span>
      <choose-field />
      <div class="buttonOp">
        <button>
          <img src="@/assets/list-icon-min.svg" alt="list_icon" />
        </button>
        <button>
          <img src="@/assets/sort-icon-min.svg" alt="sort_icon" />
        </button>
        <button>Wp</button>
      </div>
    </div>
    <file-list>
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />

      <file-list-item fName="Enwubnfjbwf" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
      <file-list-item fName="Mały plik" />
      <file-list-item fName="Skorpion" />
    </file-list>
  </div>
</template>

<style scoped>
.Buttons{
  width: 130px;
  height: 45px;
  margin-right: 90px;
  background-color: antiquewhite;
  
}

.dashboardContent {
  position: relative;
  width: 100%;
  height: 100%;
}

.Logo {
  font-size: 1.7rem;
  font-family: sans-serif;
  margin-top: 10px;
  color: rgba(0, 0, 0, 0.6);
}

.Logo > span {
  margin-left: 5px;
  font-weight: 700;
  color: rgba(30, 180, 30, 0.9);
}

.templatesDocs {
  width: 100%;
  height: 280px;
  background: rgba(230, 230, 230, 0.685);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 70px;
}

.templatesDocs_tD {
  display: flex;
  flex-direction: row;
  margin-top: 10px;
  height: 30px;
  width: 700px;
}

.templatesDocs_tD > span::first-letter {
  text-transform: uppercase;
}

.templatesDocs_tD > span {
  height: 40px;
  padding: 10px;
  margin-top: 5px;
  margin-right: 180px;
}

.templatesDocs_tD > button {
  width: 200px;
  background: transparent;
  border: none;
  outline: none;
  height: 40px;
  padding: 10px;
  margin-top: 4px;
  margin-left: 30px;
  border-radius: 4px;
  font-family: Arial, Helvetica, sans-serif, Times, serif;
  display: flex;
  justify-content: center;
  align-items: center;
}

.templatesDocs_tD > button:hover {
  background: rgba(48, 47, 47, 0.26);
}

.separator {
  width: 1px;
  height: 35px;
  background: rgba(48, 47, 47, 0.068);
  margin-top: 6px;
}

.templatesDocs_tD > .optionButton {
  width: 40px;
  background: transparent;
  border: none;
  outline: none;
  height: 40px;
  padding: 10px;
  margin-top: 4px;
  margin-left: 6px;
  border-radius: 50px;
  font-family: Arial, Helvetica, sans-serif, Times, serif;
}

.templateList {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-top: 10px;
  margin-bottom: 10px;
  height: 310px;
  width: 700px;
}

.templateItem {
  width: 114px;
  height: 190px;
  padding: 10px;
  margin: 4px;
}
/* 156 */

.templateIcon {
  width: 124px;
  height: 164px;
  border-radius: 4px;
  border: 0.3px solid rgba(47, 48, 47, 0.205);
  background: rgb(250, 250, 250);
}

.templateIcon:hover {
  border: 0.3px solid rgba(30, 180, 30, 0.9);
  cursor: pointer;
}

.templateLabel {
  font-weight: 550;
  font-size: 14px;
  overflow: hidden;
  height: 20px;
  padding-left: 4px;
  text-overflow: ellipsis;
  margin-top: 6px;
  margin-bottom: 0;
  white-space: nowrap;
}

.templateList > .templateItem > span {
  padding-left: 4px;
  font-size: 14px;
}

.lastDocs {
  display: grid;
  grid-template-columns: repeat(3, 130px);
  gap: 50vw;
  margin-top: 15px;
  height: 40px;
  width: 700px;
  margin-left: 150px;
}

.lastDocs > span {
  margin-top: 10px;
  width: 165px;
  text-align: center;
}

.lastDocs > button {
  background: transparent;
  border: none;
  outline: none;
  border-radius: 4px;
  width: 164px;
  height: 30px;
  margin-top: 5px;
}

.lastDocs > button:hover {
  background: rgba(48, 47, 47, 0.151);
}

.buttonOp {
  width: 122px;
  margin-left: 78px;
  display: flex;
  flex-direction: row;
}

.lastDocs > .buttonOp > button {
  background: transparent;
  border: none;
  outline: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.lastDocs > .buttonOp > button:hover {
  background: rgba(48, 47, 47, 0.151);
}
</style>
