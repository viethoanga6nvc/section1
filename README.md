# Ôn tập

### Javascript

- Var, let, const
- Hosting, Closure

## React

- Props:
    - Props là dữ liệu truyền từ component cha xuống component con
    - Props giúp tạo ra sự đa dạng cho component. Cùng 1 component với props khác nhau thì render ra khác nhau
- State:
    - Tạo ra và quản lý bởi component hiện tại
    - Được dùng cho những dữ liệu có khả năng sẽ thay đổi
- Ref:
    - Để “ghi nhớ” một số thông tin, nhưng bạn không muốn thông tin đó kích hoạt các kết xuất mới, bạn có thể sử dụng ref.
        - [Example](https://codesandbox.io/api/v1/sandboxes/define?parameters=N4IgZglgNgpgziAXKAggBzQOgFYOSAYwHsA7AFxnKRAgFs0iAnMgAmBYFc4YAlGMFgF8WYRkVosA5IxgBDAmUkBuADok1MAB4NmLACb9ZHKKzAcSCiKRYBhIuYqMAFAEo2ali1isZAgLyc3HxgTgAMLqrqJJ5mFmRW0QAWsiR6sDZQEAQA1q7u0Z4svpgEHIwy5CwBxaXllKwA1CwAjJGFLLKwzE6SAJr2LASZOTB6UixNNWUVjePxtPAAhJIRHkJqazJkZdFOa54APABGHGRk1qQZWdl-wMmp6cPZggB8-4VXOSwLi-8HAPQnM6kN4FVYkQRqEAAGhocAAQhASLJGABPJBgTrcQSwpEGTQ4PCgYjkerUOg6Vh8eRkaFsFgAZTIjCyZAAskQDEIRGIJCoQDIafzIhSmKx2ARBRQeEQiKxhKJxCx-YKFABaPTif5DCD1YVqUW6fmYf5wMio2BwEpwOD6qKG1joNA8pXG_5Ou1qElmoqy1gBSVyaV-pya0oLciYADmMDIAFFYBGyPDUQBJPR7AV-_kucFiOWYCoGZxrA5MlkKDkGUHtA5Olj_GssAHl1lVmCgiIwuGI5FojFYmA4kBmi3wa1EwikChURAgABU-U8RyImjVcAgAC8kVHECwV4xi2qV5pIpCoiu9KilyJp2rMbRoKi93AUnB1zAWWA2t8UVGkXuABMoRoKeaxoLIeh6Due6hGeGwkIkzQ3rQf5Imq5xoLBP5gHeG6bjAQGAaB8FRIkgEoWhJAYUQWEsHBay4eQ65boRLDASRajnmoiQAMyUYw_7UZh2GMXhrF7s0AAcnEQghiQACwCUJNF0QxBRMWQLEEZJABssncYhACsynoSJ9E4eJOktApBnybppnCbRokaVZbHNMRYFyVExBcsAYnMfh7mYIBMC0KRajGDeEFQTuapIpkJAwOuZAomQQEgV5hndhACJIii6KIJiUDYrCaAcEcwz_HiWiYIkZC0FASDEtOZJzgciwACIAPI2AAKr0AAKcYsPVjWggcY1QF4KRRn4_KUPyTaTXIehNocCypYMySMNwZDzSAACqfUAGJqlJS1_JtsgsMiCwHQAbrqADulL8oMrXkAdz0QHoZCJH4BhPQQyU_X9iR0kiEDxJ064EJ0MB-M0mChJdBSHPEZCwC8nVEOG9QApj2Olv8iSrctl6outzbQQ9LC_Qd-ZkEtAK08tgKclTagAlNLw5XlfaFcVpUgBBOSyDGhKkM1U6krOID-QU_IGGglAGBYuq2kgN6eCqcgKPye78gAetJKMo_y0LvHrNIauIhvKiAptSebqMwtbAr61pcCShAaBkFrRtO0Zrv8msOJrPyqFIg7_LVaktW4JbkcgEDnUwKrCca_ADvAOegj872BUDiVQ7DhQ9BQLIFDUIG1fJaqWmyBgICCEAA&query=file%3D%252FApp.js%26utm_medium%3Dsandpack)
        
        ```jsx
        import { useRef } from 'react';
        
        export default function Counter() {
          let ref = useRef(0);.
        
          function handleClick() {
            ref.current = ref.current + 1;
            alert('You clicked ' + ref.current + ' times!');
          }
        
          return (
            <button onClick={handleClick}>
              Click me!
            </button>
          );
        }
        ```
        
    - Cần quyền truy cập vào các phần tử DOM do React quản lý—ví dụ: để tập trung vào một Node, cuộn đến Node đó hoặc đo kích thước và vị trí của Node đó
        - [Example](https://codesandbox.io/api/v1/sandboxes/define?parameters=N4IgZglgNgpgziAXKAggBzQOgFYOSAYwHsA7AFxnKRAgFs0iAnMgAmBYFc4YAlGMFgF8WYRkVosA5IxgBDAmUkBuADok1MAB4NmLACb9ZHKKzAcSCiKRYAxJrQAUASjZqWLYiTisIJNBzI-AQBeTm4ghxJjKCdVdRJ3MwsyKwSAC1kSPVgAYSgIAgBrZ1cE9xZff0D-TAIORhlyTDAiOrhnOPdBNTcWGTJ6hIde9wAeAD4R8tHKgL7-YOBZ6rBhAHpJsvKWUYAjALJrUjyCwsWMrNz8osFN7e27NpYyNJgKvwCpsbX9skOSO7TDa9WJqbokEAAGhocAAQr5ZIwAJ5IMCyKDcQTQ3wGTQ4PCgTwUKiIGj0JisPjyMiQtgsADKZEYBTIAFkiAYhCIxBIVCAZNS-XE6DpWOwCAKKDwiERWMJROIWHyBQoALR6cRrAj5ShkIVqEUUpUgTBrbxI2BwWpwOD6-KG3ToNDcxV801Ou1qTzePoy1ihCVyKV-hwauq0XWYADmMDIAFFYBHyLCkQBJPTDfl-vlOUEkMSyzCNAyMYZlUaM5kKdkGQFjJ0sYHltaVlk1mCbWJQmHwkiIlGINEYmBYkDmy3WgmEUjEsjUABUpXcuyImlVcAgAC9fFHECwV4wS6qV5o4uC1Cu9EilyIZ6q0bRoEi93BMnB1zBmWBOixaIio74e4AEwAAxoKevRoLIeh6Due4gWePQkGkACMN5_owAEkKqhxoPBP4tOQ65bjAwFAeBiHxGkQHof-vg4UQeEsAhvSEWQxGbqRLCgRRYJIWkADMtGYfRuH4axd4bpxe4oQAHLxJDnshAAswlYQxTEsWUbEcVxKEAGwKUpaQAKxqaJjHidpkkkTJylGfx-nmdhYnMQRNnSSwKHkRBilIcQnLABJRFSXpmBATAtCUWoxg3lBME7qqvj5CQMDrmQiJkMBYG-Up3YQHCCLIqi6KYtC_i7Ncaw4lomBpGQtBQEghIzrq1CjAAhAAIgA8jkAAqACaAAKcYsPVjWbKME1QCwUCZFGwR8pQfKAtNch6HWOwRhlHgZIw3BkEtIAAKr9TYqqyatUyjDtsgsH2EbHQAbhAMAAO6inyHiteQx3vRAegvMEBivQQaUA0DaS0r4EApOi64EOiMDBChmAgddWw7CkZCwOMXWtBwSZkKMaw43jvSk680FrZeSJbaMsHPRUejHQWeogOMpNM2tPwcvTahUw1UDjPlhV9sVg6lSO5XyIUsgxvipDNdO5BtaSQVlHyBhoJQBgWG9tpIDe7jKnICh8nufIAHpyej6N8pCUxm9S6riJbxq27J9sY1Czv8ub7FwBKEBoGQRtWyA1smT7fK9FivR8n-vge3y1VZLVuCO4nICg11MC6xnBvwB7wDgoIYu9v2JXDoIo4UPQ80UNQgayBQqoquxsgYCAghAA&query=file%3D%252FApp.js%26utm_medium%3Dsandpack)
        
        ```jsx
        import { useRef } from 'react';
        
        export default function Form() {
          const inputRef = useRef(null);
        
          function handleClick() {
            inputRef.current.focus();
          }
        
          return (
            <>
              <input ref={inputRef} />
              <button onClick={handleClick}>
                Focus the input
              </button>
            </>
          );
        }
        ```
        
- React List, key
    - Key cho React biết mỗi thành phần tương ứng với mục mảng nào để nó có thể khớp với chúng sau này. Điều này trở nên quan trọng nếu các mục trong mảng của bạn có thể di chuyển (ví dụ: do sắp xếp), được chèn vào hoặc bị xóa. Key được chọn tốt sẽ giúp React suy ra chính xác điều gì đã xảy ra và thực hiện cập nhật chính xác cho cây DOM.
    - Hãy tưởng tượng rằng các tập tin trên màn hình của bạn không có tên. Thay vào đó, bạn sẽ đề cập đến chúng theo thứ tự - tệp đầu tiên, tệp thứ hai, v.v. Bạn có thể quen với nó, nhưng một khi bạn xóa một tập tin, nó sẽ trở nên khó hiểu. Tệp thứ hai sẽ trở thành tệp đầu tiên, tệp thứ ba sẽ là tệp thứ hai, v.v.↳
    - Tên tệp trong một thư mục và các khóa JSX trong một mảng đều phục vụ mục đích tương tự. Họ cho phép chúng tôi xác định duy nhất một mục giữa anh chị em của nó. Khóa được chọn tốt sẽ cung cấp nhiều thông tin hơn vị trí trong mảng. Ngay cả khi vị trí thay đổi do sắp xếp lại, khóa vẫn cho phép React xác định mục trong suốt vòng đời của nó
- Life cycle
    - Được tạo ra (Mounting)
    - Qua nhiều thay đổi (Updating)
    - Và bị huỷ bỏ (Unmouting)
- hook: useEffect, useMemo, useCallback
    - useEffect:
        - 2 loại side effect:
            - Effect không cần clean up: gọi API, tương tác với DOM
            - Effect cần clean up: setTimeout, setInterval, subscription
        - useEffect:
            - Là một hook cơ bản
            - Sử dụng cho side effect
            - Mỗi hook gồm 2 phần side effect và clean up (optional)
            - Được thực thi sau mỗi lần render
            - Được thực thi ít nhất 1 lần sau lần render đầu tiên
            - Những lần render sau, chỉ được thực thi nếu có dependencies thay đổi
            - Effect cleanup sẽ được thực thi trước run effect tiếp theo hoặc unmount
            - Có thể dùng nhiều useEffect
        
        ```jsx
        // callback: Your side effect function
        // dependencies: Only execute callback if one of your dependencies changes
        function useEffect(callback, dependencies) {}
        
        function App() {
          // executed before each render
          const [color, setColor] = useState('deeppink');
          // executed after each render
        useEffect(() => {
        // do your side effect here ...
        return () => {
        // Clean up here ...
        // Executed before the next render or unmount
        }; }, []);
        // rendering
          return <h1>Easy Frontend</h1>;
        }
        
        MOUNTING
        - rendering
        - run useEffect()
        UPDATING
        - rendering
        - run `useEffect() cleanup` nêu dependencies thay đôi.
        ́̉
        - run `useEffect()` nêu dependencies thay đôi.
        UNMOUNTING
        - run `useEffect() cleanup`.
        ```
        
        ```jsx
        function App() {
          const [filters, setFilters] = useState();
          useEffect(() => {
            // EVERY
            // No dependencies defined
            // Always execute after every render
        return () => {
        // Execute before the next effect or unmount.
        }; });
          useEffect(() => {
            // ONCE
            // Empty dependencies
            // Only execute once after the FIRST RENDER
            return () => {
              // Execute once when unmount
        }; }, []);
          useEffect(() => {
            // On demand
            // Has dependencies
            // Only execute after the first RENDER or filters state changes
        return () => {
        // Execute before the next effect or unmount.
            };
          }, [filters]);
        }
        ```
        
        - Dùng Effect không có cleanup
        
        ```jsx
        function App() {
          const [postList, setPostList] = useState([]);
          useEffect(() => {
            async function fetchData() {
              try {
                // TODO: Should split into a separated api file instead of using
        fetch directly
        const queryParamsString = queryString.stringify();
        const requestUrl = `http://js-post-api.herokuapp.com/api/posts? _limit=10`;
        const response = await fetch(requestUrl); const responseJSON = await response.json(); const { data, pagination } = responseJSON;
        console.log({ data, pagination });
                setPostList(data);
              } catch (error) {
        console.log('Failed to fetch posts: ', error.message); }
        }
            fetchData();
          }, []);
        return <div>Post list length: {postList.length}</div>; }
        ```
        
        - Dùng Effect có cleanup
        
        ```jsx
        function Clock() {
          const [timeString, setTimeString] = useState(null);
          const intervalRef = useRef(null);
        useEffect(() => {
        intervalRef.current = setInterval(() => {
        const now = new Date();
        const hours = `0${now.getHours()}`.slice(-2);
        const minutes = `0${now.getMinutes()}`.slice(-2);
        const seconds = `0${now.getSeconds()}`.slice(-2);
        const currentTimeString = `${hours}:${minutes}:${seconds}`;
              setTimeString(currentTimeString);
            }, 1000);
        return () => { clearInterval(intervalRef.current);
        }; }, []);
          return (
            <div style={{ fontSize: '48px' }}>{timeString}</div>
        ); }
        ```
        
- Redux:
    - Store gồm có:
        - State: là dữ liệu hiện tại được lưu trên state
        - Reducer: là hàm biến đổi state cũ sang state mới
        - Dispatcher: quản lý middlewares và chuyền dữ liệu xuống reducer
    - Action: plain javascript object mô tả hành động
    - Khi nào dùng redux
        - Dữ liệu được lưu ở nhiều nơi
