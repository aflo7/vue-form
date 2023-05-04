<script setup></script>

<template>
    <div class="form-wrapper">
        <h2>Voice Provisioning</h2>

        <form>
            <div style="display: flex; padding: 10px">
                <select
                    name="partner"
                    id="partner"
                    style="flex: 1; padding: 10px; padding-left: 15px"
                >
                    <option value="sprout">Sprout</option>
                    <option value="option2">Option 2</option>
                    <option value="option3">Option 3</option>
                </select>
            </div>

            <div style="display: flex; padding: 10px; margin-top: 20px">
                <input
                    type="text"
                    placeholder="Account Number"
                    style="flex: 1"
                />
            </div>

            <div
                style="
                    display: flex;
                    gap: 25px;
                    padding: 10px;
                    margin-top: 20px;
                "
            >
                <input type="text" placeholder="First Name" style="flex: 1" />
                <input type="text" placeholder="Last Name" style="flex: 1" />
            </div>

            <div class="row-4">
                <input type="text" placeholder="Address" />
                <input type="text" placeholder="City" />
                <input type="text" placeholder="State" />
                <input type="text" placeholder="Zip" />
            </div>

            <div
                style="
                    display: flex;
                    gap: 25px;
                    padding: 10px;
                    margin-top: 20px;
                "
            >
                <input
                    type="text"
                    placeholder="Contact Phone"
                    style="flex: 1"
                />
                <input
                    type="text"
                    placeholder="Contact Email"
                    style="flex: 1"
                />
            </div>

            <div
                style="
                    display: flex;
                    gap: 25px;
                    padding: 10px;
                    margin-top: 20px;
                "
            >
                <select style="flex: 1; padding: 10px">
                    <option value=""></option>
                </select>

                <input
                    type="text"
                    placeholder="Phone Number to Provision"
                    style="flex: 1"
                />
                <input type="text" placeholder="Sip Password" style="flex: 1" />
            </div>

            <div style="display: flex; padding: 10px; margin-top: 20px">
                <select style="width: 33%; padding: 10px">
                    <option value=""></option>
                </select>
            </div>

            <div class="e911-wrapper">
                <label class="e911-label">
                    <div>
                        <input type="checkbox" />
                        <span style="padding-left: 15px"
                            >Bypass E911 Address Automation</span
                        >
                    </div>
                </label>

                <div class="bypass-info">
                    <div>
                        <i class="bi bi-info-circle-fill caution-icon"> </i>
                    </div>

                    <div>
                        (By checking "Bypass E911 Address Automation" you agree
                        to manually add this phone number and address to
                        Bandwidth)
                    </div>
                </div>
            </div>

            <div class="provision-btn-wrapper">
                <button type="submit">PROVISION</button>
            </div>
        </form>
    </div>
</template>

<style scoped>
.form-wrapper {
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    align-items: center;
}

form {
    width: 1040px;
}

input {
    background-color: rgb(234, 242, 249);
    border-radius: 5px;
    border: none;
    padding: 10px;
    padding-left: 20px;
    box-shadow: 0 2px 3px rgba(0, 0, 0, 0.5);
}

input[type="checkbox"] {
    box-shadow: none;
}

select {
    background-color: rgb(234, 242, 249);
    border-radius: 5px;
    border: none;
    box-shadow: 0 2px 3px rgba(0, 0, 0, 0.5);
    border-right: 20px solid transparent;
}

.provision-btn-wrapper {
    padding: 20px;
}

.row-4 {
    display: flex;
    gap: 25px;
    padding: 10px;
    margin-top: 20px;
}

.row-4 div {
    flex-grow: 1;
}

.provision-btn-wrapper > button {
    background-color: rgb(35, 29, 108);
    color: white;
    padding: 5px 20px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    box-shadow: 0 2px 3px rgba(0, 0, 0, 0.5);
}

.bypass-info {
    outline: 1px solid rgb(237, 129, 39);
    border-top: 10px solid rgb(246, 205, 165);
    color: rgb(237, 129, 39);
    width: 60%;
    display: flex;
    flex-direction: row;
    padding: 10px;
    padding-left: 20px;
    gap: 20px;
    border-radius: 10px;
}

.e911-label {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.e911-wrapper {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    margin-top: 20px;
}
</style>
